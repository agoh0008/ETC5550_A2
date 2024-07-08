---
title: "Assignment 3"
author: "Alexandra Goh (29796431)"
output: 
  bookdown::html_document2: 
    keep_md: true
date: "2024-03-30"
---
<br>





#### **Using a test set of 2018–2022, fit an ETS model chosen automatically, and three benchmark methods to the training data. Which gives the best forecasts on the test set, based on RMSE?**

Figure \@ref(fig-1) shows the population trend in Kiribati from 1960 to 2022.


![](Assignment3_29796431_files/figure-html/fig-1-1.png)<!-- -->





<table class="table" style="width: auto !important; margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> .model </th>
   <th style="text-align:left;"> Country </th>
   <th style="text-align:left;"> .type </th>
   <th style="text-align:right;"> ME </th>
   <th style="text-align:right;"> RMSE </th>
   <th style="text-align:right;"> MAE </th>
   <th style="text-align:right;"> MPE </th>
   <th style="text-align:right;"> MAPE </th>
   <th style="text-align:right;"> MASE </th>
   <th style="text-align:right;"> RMSSE </th>
   <th style="text-align:right;"> ACF1 </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> ETS(log(Population)) </td>
   <td style="text-align:left;"> Kiribati </td>
   <td style="text-align:left;"> Test </td>
   <td style="text-align:right;"> 481.4085 </td>
   <td style="text-align:right;"> 642.2875 </td>
   <td style="text-align:right;"> 481.4085 </td>
   <td style="text-align:right;"> 0.3721635 </td>
   <td style="text-align:right;"> 0.3721635 </td>
   <td style="text-align:right;"> NaN </td>
   <td style="text-align:right;"> NaN </td>
   <td style="text-align:right;"> 0.4368641 </td>
  </tr>
</tbody>
</table>

<table class="table" style="width: auto !important; margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> .model </th>
   <th style="text-align:left;"> Country </th>
   <th style="text-align:left;"> .type </th>
   <th style="text-align:right;"> ME </th>
   <th style="text-align:right;"> RMSE </th>
   <th style="text-align:right;"> MAE </th>
   <th style="text-align:right;"> MPE </th>
   <th style="text-align:right;"> MAPE </th>
   <th style="text-align:right;"> MASE </th>
   <th style="text-align:right;"> RMSSE </th>
   <th style="text-align:right;"> ACF1 </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> MEAN(log(Population)) </td>
   <td style="text-align:left;"> Kiribati </td>
   <td style="text-align:left;"> Test </td>
   <td style="text-align:right;"> 49333.290 </td>
   <td style="text-align:right;"> 49436.633 </td>
   <td style="text-align:right;"> 49333.290 </td>
   <td style="text-align:right;"> 38.924654 </td>
   <td style="text-align:right;"> 38.924654 </td>
   <td style="text-align:right;"> NaN </td>
   <td style="text-align:right;"> NaN </td>
   <td style="text-align:right;"> 0.4072310 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> NAIVE(log(Population)) </td>
   <td style="text-align:left;"> Kiribati </td>
   <td style="text-align:left;"> Test </td>
   <td style="text-align:right;"> 6193.047 </td>
   <td style="text-align:right;"> 6955.845 </td>
   <td style="text-align:right;"> 6193.047 </td>
   <td style="text-align:right;"> 4.831340 </td>
   <td style="text-align:right;"> 4.831340 </td>
   <td style="text-align:right;"> NaN </td>
   <td style="text-align:right;"> NaN </td>
   <td style="text-align:right;"> 0.4072892 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> RW(Population ~ drift()) </td>
   <td style="text-align:left;"> Kiribati </td>
   <td style="text-align:left;"> Test </td>
   <td style="text-align:right;"> 2395.937 </td>
   <td style="text-align:right;"> 2764.957 </td>
   <td style="text-align:right;"> 2395.937 </td>
   <td style="text-align:right;"> 1.866105 </td>
   <td style="text-align:right;"> 1.866105 </td>
   <td style="text-align:right;"> NaN </td>
   <td style="text-align:right;"> NaN </td>
   <td style="text-align:right;"> 0.4148619 </td>
  </tr>
</tbody>
</table>





#### **Check the residuals from the best model using an ACF plot and a Ljung-Box test. Do the residuals appear to be white noise?**


#### **Now use time-series cross-validation with a minimum sample size of 15 years, a step size of 1 year, and a forecast horizon of 5 years. Calculate the RMSE of the results. Does it change the conclusion you reach based on the test set?**


#### **Which of these two methods of computing accuracy is more reliable? Why?**

