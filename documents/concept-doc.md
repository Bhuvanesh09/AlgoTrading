# Project Concept Document

| Field          | Value                                                                 |
| -------------- | --------------------------------------------------------------------- |
| Project number | 13                                                                    |
| Project Title  | Algorithmic Trading                                                   |
| Document       | DASS Project Concept Document                                         |
| Creation date  | January 21, 2020                                                      |
| Created By     | Animesh Sinha, Bhuvanesh Sridharan, Gadela Kesav, L. Sai Tharun Reddy |
| Client         | Spinlogics                                                            |


## Description

+   To develop an Algorithmic Trading script which uses data obtained from the web (currently using a library called Binance on Cryptocurrencies)
+   Algorithm also suggests whether or not to invest
+   And in what to invest / pull out of.
+   We are to use classical measures like Exponentially Weighted Averages, Simply Weighted Averages, etc. over different timescales, and construct market indicators out of these combinations.
+   Our end goal is to research and try out combination of these parameters in code and be able to make reasonably good predictions of the trend in the prices of any cryptocurrency.
+   Further, if time permits, a convonutional neural network is to be programmed and trained over the data collected all this time.
+   The prediction of the neural net is to be compared with the performance of classical measures.

## Profile of Users


+ The script will be used by people who are working to invest or trade in Cryptocurrencies. 
+ This script is to act as a foray into the possibilities of such an algorithmic trading approach by the company Spinlogics, therefore we are not tasked with building a User Interface. Comparative study and Evaluation of different indicators, metrics and models by Spinlogics shall be the primary goal of the project.
+ The profile of the user also ranges from machine learning experts and analysts who wish to study the effectiveness of such an aproach.

## Usage Model and Diagrams (if any)

The Script will be generating alerts for it's users on Telegram about any notable trend which it predicts by messaging them directly. Both the alert and preferrably the reasoning behind the alert (Graphs / Indicators that led to the program flagging the time) will be shared with the user. The script must also log all its past predictions and their accuracy in an XML/csv format for further analysis by the user.