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

* An internet speed monitoring app built in the Shiny web framework for R. 
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

## Slide 4

---

## Slide 5




