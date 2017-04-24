pollutantmean <- function(directory, pollutant, id = 1:332){
        data <- numeric()
        for (i in id) {
                readFile <- read.csv(paste(directory, "/", formatC(i, width = 3, flag = "0"), ".csv", sep = ""))
                data <- c(data, readFile[[pollutant]])
        }
        mean(newData, na.rm = TRUE)
}

pollutantmean("specdata", "nitrate", 23) 
## 1.281
pollutantmean("specdata", "sulfate", 1:10)
## 4.064
pollutantmean("specdata", "nitrate", 70:72)
## 1.706
