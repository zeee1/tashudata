Installation : “tashudata” package
----------------------------------

Package ‘tashudata’ should be installed by using ‘drat’ package before
calling analysis function. tashudata contains some data such as bicycle
rental history, weather and bicycle station information for 3 years.
Functions of package ‘tashu’ uses data on ‘tashudata’.

    library(drat)
    addRepo("zeee1")
    install.packages("tashudata")

    library(tashudata)

Data
----

Package ‘tashudata’ provides 3 types of dataset.

1.  Tashu Data  
    Bicycle rental history on Tashu from 2013 to 2015. Data is consisted
    of “RENT STATION, RENT DATE, RETURN STATION, RETURN DATE”

-   tashu : Rental/Return record from 2013 to 2015.

<!-- -->

    head(tashudata::tashu, n = 5)

    ##   RENT_STATION           RENT_DATE RETURN_STATION         RETURN_DATE
    ## 1           43 2013-01-01 05:56:03             34 2013-01-01 06:02:17
    ## 3            2 2013-01-01 06:04:06             10 2013-01-01 06:18:59
    ## 4          106 2013-01-01 10:53:05            105 2013-01-01 10:57:43
    ## 5            4 2013-01-01 11:22:23              4 2013-01-01 12:17:53
    ## 6           21 2013-01-01 11:39:53            105 2013-01-01 11:49:43

1.  Tashu Station Data  
    By 2014 there were 144 bicycle stations on “Tashu” system. In this
    package, only the existing data of 144 stations are considered. Data
    is consisted of “NUM(Number of station), NUMOFBIKE\_RACK(Number of
    Bike rack), GEODATA\_lat(Latitude of station),
    GEODATA\_lon(Longitude of station)”

-   tashuStation : data of 144 Stations on Tashu system.

<!-- -->

    head(tashudata::tashuStation, n = 5)

    ##   NUM NumOFBIKE_RACK GEODATA_lat GEODATA_lon
    ## 1   1             14    36.37432    127.3875
    ## 2   2             20    36.37447    127.3922
    ## 3   3             19    36.36986    127.3887
    ## 4   4             12    36.36819    127.3793
    ## 5   5             13    36.36503    127.3894

1.  Weather Data  
    Weather data In Daejeon from 2013 to 2015. It is consisted of
    “datetime, temperature, rainfall, windspeed, wind direction,
    humidity, Dew point temperature, Local Pressure, Sea surface
    Pressure, Sunshine, Solar Radiation, Snowfall, Ground Temperature”

-   weather : weather data in Daejeon from 2013 to 2015

<!-- -->

    head(tashudata::weather, n = 5)

    ##              Datetime Temperature Rainfall WindSpeed WindDirection
    ## 1 2013-01-01 00:00:00        -8.8       NA       0.1             0
    ## 2 2013-01-01 01:00:00        -8.5       NA       0.9           270
    ## 3 2013-01-01 02:00:00        -8.5       NA       1.0           320
    ## 4 2013-01-01 03:00:00        -9.0       NA       0.7           270
    ## 5 2013-01-01 04:00:00        -9.1       NA       0.6           320
    ##   Humidity VaporPressure DewpointTemperature LocalPressure
    ## 1       90           2.8               -10.1        1013.3
    ## 2       90           2.9                -9.8        1013.2
    ## 3       89           2.9                -9.9        1012.6
    ## 4       91           2.8               -10.2        1012.5
    ## 5       92           2.8               -10.1        1011.4
    ##   SeaSurfacePressure Sunshine SolarRadiation Snowfall GroundTemperature
    ## 1             1022.3       NA             NA      8.8              -0.9
    ## 2             1022.2       NA             NA      8.8              -0.8
    ## 3             1021.6       NA             NA      8.8              -0.8
    ## 4             1021.5       NA             NA      8.8              -0.8
    ## 5             1020.4       NA             NA      8.8              -0.8
    ##   X5cmGroundTemperature X10cmGroundTemperature X20cmGroundTemperature
    ## 1                  -0.1                    0.3                    1.1
    ## 2                  -0.1                    0.3                    1.1
    ## 3                  -0.1                    0.3                    1.1
    ## 4                  -0.1                    0.3                    1.1
    ## 5                  -0.1                    0.3                    1.1
    ##   X30cmGroundTemperature
    ## 1                    1.5
    ## 2                    1.5
    ## 3                    1.4
    ## 4                    1.5
    ## 5                    1.5
