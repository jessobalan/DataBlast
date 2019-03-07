# "Flight Landing Analysis using linear, logistic and multinomial regression"
#### Author: Anthony Selva Jessobalan
#### Date: March 7, 2019

## Background

This is a study to see what factors and how would they affect the landing distance of commerical flights. The data used here is a simulated data from statistical models. The motivation behind the study is to reduce the risk of [landing overruns](https://en.wikipedia.org/wiki/Category:Airliner_accidents_and_incidents_involving_runway_overruns). See two CSV files used as data source here: 

<https://github.com/jessobalan/Flight-Landing-Analysis/blob/master/FAA1.csv> 

<https://github.com/jessobalan/Flight-Landing-Analysis/blob/master/FAA2.csv>. 

FAA1 has 800 data points and FAA2 has 150 data points.

### Variable Dictionary:

**Aircraft**: The make of an aircraft (Boeing or Airbus). 
**Duration (in minutes)**: Flight duration between taking off and landing. The duration of a normal flight should always be greater than 40min.  
**No_pasg**: The number of passengers in a flight.  
**Speed_ground (in miles per hour)**: The ground speed of an aircraft when passing over the threshold of the runway. If its value is less than 30MPH or greater than 140MPH, then the landing would be considered as abnormal.  
**Speed_air (in miles per hour)**: The air speed of an aircraft when passing over the threshold of the runway. If its value is less than 30MPH or greater than 140MPH, then the landing would be considered as abnormal.  
**Height (in meters)**: The height of an aircraft when it is passing over the threshold of the runway. The landing aircraft is required to be at least 6 meters high at the threshold of the runway.  
**Pitch (in degrees)**: Pitch angle of an aircraft when it is passing over the threshold of the runway.  
**Distance (in feet)**: The landing distance of an aircraft. More specifically, it refers to the distance between the threshold of the runway and the point where the aircraft can be fully stopped. The length of the airport runway is typically less than 6000 feet.  

#### Reading CSVs into R

```{r import, echo=TRUE}
FAA1<-read.csv("Flight-Landing-Analysis/FAA1.csv ",header=T)
FAA2<-read.csv("Flight-Landing-Analysis/FAA2.csv ",header=T)
```

## Including Plots

You can also embed plots, for example:

```{r pressure, echo=FALSE}
plot(pressure)
```

Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.
