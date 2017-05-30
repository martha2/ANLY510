# ANLY510
Question 1--
> require(zoo)
> dat2=transform(dirty_data,Area=na.locf(Area))
Question 2--
dat2$Street=gsub("[^[:alnum:]///' ]", "", dat2$Street)
dat2$Street.2=gsub("[^[:alnum:]///' ]", "", dat2$Street.2)
dat2$Street.2=gsub(" ", "", dat2$Street.2)
dat2$Street <- gsub("^(\\w)(\\w+)", "\\U\\1\\L\\2", dat2$Street, perl = TRUE)
dat2$Street.2 <- gsub("^(\\w)(\\w+)", "\\U\\1\\L\\2", dat2$Street.2, perl = TRUE)

