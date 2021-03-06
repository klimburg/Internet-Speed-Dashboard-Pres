---
title       : Home Internet Speed Dashboard
subtitle    : A web app for monitoring home internet speeds
author      : Kevin C. Limburg
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

<!-- Limit image width and height -->
<style type='text/css'>
img {
    max-height: 500px;
    max-width: 800px;
}
</style>

<!-- Center image on slide -->
<script src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.7.min.js"></script>
<script type='text/javascript'>
$(function() {
    $("p:has(img)").addClass('centered');
});
</script>    

## Introduction

* An [internet speed monitoring app](https://klimburg.shinyapps.io/InternetSpeedDash/) built in the Shiny web framework for R. 
* The data is collected using [Janhouse/tespeed](https://github.com/Janhouse/tespeed) python tool which allows internet speed testing via http://www.speedtest.net from a command line interface.
* This application was built as a project for the Coursera Data Science Specialization Developing Data Products class.
* The source files can all be found at [https://github.com/klimburg/InternetSpeedDash](https://github.com/klimburg/InternetSpeedDash).

---

## Features

* Application displays time series and histogram of download and upload speeds.
* Filterable by date, internet plan speed and server.

![screenCap](assets/img/ScreenCap.png)


---

## Compare Actual vs. Advertised 

* Do you wonder if you are getting the speeds that you pay for?
* Compare actual vs. advertised speeds

![compare plans](assets/img/ComparePlans.png)


---

## Limitations

It should be noted that other factors besides the advertised speed of your internet plan may affect the recorded speeds, such as the server responsible for the content.

An example of this can be seen when looking at the speeds by server when I had Comcast's 25 Mbit/Sec download speed. 


![boxplot](assets/img/boxplot1.png)

The plot shows that the chi.ookla.towerstream.net server behaves differently from the rest, with a median download speed of 10.41 Mb/s while the others have median values of approximately 30 Mb/s. 

---

## Future Improvements

Many improvements could be added to improve this application:
* Add a predictive forecast for future speeds, factors could include day of the week and time of day.
* Add boxplots and other exploratory analysis tools

Some improvements would require more modifications of tespeed.py or the cronjob running it
* Track ping speed
* Take measurements from multiple servers on each attempt to allow comparisions across servers at the same time


