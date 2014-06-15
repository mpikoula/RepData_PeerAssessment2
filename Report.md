# The impact of Storms and other severe weather events on public health and the economy of the United States

## Synopsis

## Data Processing

Loading the data:


```r
#First find out how many columns are included:
stormy <- read.csv("repdata-data-StormData.csv", nrows=1)
head(stormy)
```

```
##   STATE__          BGN_DATE BGN_TIME TIME_ZONE COUNTY COUNTYNAME STATE
## 1       1 4/18/1950 0:00:00      130       CST     97     MOBILE    AL
##    EVTYPE BGN_RANGE BGN_AZI BGN_LOCATI END_DATE END_TIME COUNTY_END
## 1 TORNADO         0      NA         NA       NA       NA          0
##   COUNTYENDN END_RANGE END_AZI END_LOCATI LENGTH WIDTH F MAG FATALITIES
## 1         NA         0      NA         NA     14   100 3   0          0
##   INJURIES PROPDMG PROPDMGEXP CROPDMG CROPDMGEXP WFO STATEOFFIC ZONENAMES
## 1       15      25          K       0         NA  NA         NA        NA
##   LATITUDE LONGITUDE LATITUDE_E LONGITUDE_ REMARKS REFNUM
## 1     3040      8812       3051       8806      NA      1
```

```r
#classes <- sapply(storms,class)
#classes
#We are going to keep "EVTYPE", "FATALITIES", "INJURIES", "PROPDMG", "CROPDMG"

storms <- read.csv("repdata-data-StormData.csv",colClasses = c(rep("NULL", 7), "factor", rep("NULL",14), rep("numeric",3), "factor", "numeric", "factor", rep("NULL", 9), skip=600000, nrows=1232705))
```

```
## Warning: cols = 37 != length(data) = 39
```

```r
head(storms)
```

```
##    EVTYPE FATALITIES INJURIES PROPDMG PROPDMGEXP CROPDMG CROPDMGEXP
## 1 TORNADO          0       15    25.0          K       0           
## 2 TORNADO          0        0     2.5          K       0           
## 3 TORNADO          0        2    25.0          K       0           
## 4 TORNADO          0        2     2.5          K       0           
## 5 TORNADO          0        2     2.5          K       0           
## 6 TORNADO          0        6     2.5          K       0
```
## Results

## Conclusions
