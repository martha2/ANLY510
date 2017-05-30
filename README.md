# ANLY510
Github homework--


Question 1--
> require(zoo)
> dat2=transform(dirty_data,Area=na.locf(Area))

Question 2--
dat2$Street=gsub("[^[:alnum:]///' ]", "", dat2$Street)
dat2$Street.2=gsub("[^[:alnum:]///' ]", "", dat2$Street.2)
dat2$Street.2=gsub(" ", "", dat2$Street.2)
dat2$Street <- gsub("^(\\w)(\\w+)", "\\U\\1\\L\\2", dat2$Street, perl = TRUE)
dat2$Street.2 <- gsub("^(\\w)(\\w+)", "\\U\\1\\L\\2", dat2$Street.2, perl = TRUE)

Question 3--
dat3=dat2
dat3[,4][dat3[,3]==dat3[,4]]<-NA


Question 4--
install.packages("dplyr")
library("dplyr")
dat4=select(dat3,-Strange.HTML)



