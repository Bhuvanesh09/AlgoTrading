## Product Design

Team 36: Bhuvanesh Sridharan, Animesh Sinha, Kesav Gadela, Sai Tarun Reddy

## Design Overview

### Architectural design

The Segment of our analysis and code are relatively separate and functionally independent. We shall develop the entire code on Python using the existing Rule based code and adding in Python and developing Neural Nets in PyTorch / Tensorflow.

## System interfaces

### User Interface

There is no direct user interface, only a Telegram messaging bot which sends notifications with `/buy` or `/sell` tags as advice to the user. It attaches the rule that raised the flag and graphs for detail.

| Class       | Information                                                       |
| ----------- | ----------------------------------------------------------------- |
| DataGrabber | Keeps the data on CryptoCurrencies and their value history.       |
|             | Queries the binance data. Exposes get_price(date, coin) function  |
|             | to access price of coins. Caches data being saved to a local      |
|             | database                                                          |
| Messages    | Exposes the telegram message sending API via a wrapper.           |
|             | send_message(message, tag, image) will be the function to call,   |
|             | allows you to send graph as well.                                 |
| Predictors  | Classes that help predict the market going up or down.            |
|             | 1. Rule Based                                                     |
|             | 2. ML Model                                                       |
|             | 3. Pump Detect                                                    |
|             | All these have a predict function, they keep a DataGrabber object |
|             | and you get UP/DOWN as output                                     |
| Advisor     | Takes an array of predictors and a Messages client and gives      |
|             | `/buy` or `/sell` as output.                                      |

## Sequence Diagram(s)

![UseCase Diagram](../diagrams/usecase-diagram.png)

## Design Rationale

The Project has been split into 3 ordered phases
1. Rule Based Algorithms - Comparison
2. Pump Detection by statiscal means
3. Machine Learning Models (Convolution Nets)

These 3 phases are ordered such because the results of one can feed features into the next stage of the pipeline.