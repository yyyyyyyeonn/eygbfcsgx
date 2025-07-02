freq <- read.csv("0301.frequency.csv", 
                 header=TRUE, 
                 na.strings = ".")
freq$grade <- factor(freq$grade, 
                     levels=c(1:5),
                     labels=c("F","D","C","B","A"))
str(freq)


attach(freq)

##02.일변량 범주형 자료
barplot(grade)

#그래프 에러(table로 정리한 후에 연결-원자료 사용 못함)
#기본 막대그래프
grade <- table(grade)
barplot(grade)

