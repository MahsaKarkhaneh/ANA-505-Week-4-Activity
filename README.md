# ANA-505-Week-4-Activity
hw1 <- getwd()
setwd(dir=hw1)
HairEyeColor
Mydata <- HairEyeColor
Mydata
head(Mydata,1)
install.packages(package="dplyr")
library(package="dplyr")
Mydata<- as.data.frame(Mydata)
select(.data = Mydata,c(1,3))
hair_sex <- select(.data = Mydata,c(1,3))
hair <-  select(.data = hair_sex,-Sex)
hair
Mydata1 <- rename(.data = Mydata,gender= Sex)
Mydata1
males <- filter(.data = Mydata1, gender=="Male")
males
Mydata1 %>%
  group_by(gender)%>%
  print()
total=mutate(Mydata1, total=cumsum(Freq))
total
#After you run it, write the total here:_592_
females <- filter(.data = Mydata1, gender=="Female")
females
bind_rows(males,females)
glimpse(Mydata1)

[week4.txt](https://github.com/MahsaKarkhaneh/ANA-505-Week-4-Activity/files/9227987/week4.txt)
