# Overview
This project is a sample that helps to showcase how Spring supports [Amazon Simple Queue Service (SQS)](https://aws.amazon.com/sqs/).  Every second a simple payload is placed on the queue which a consumer should immediately process.

# Guidebook
Details about this project are contained in the [guidebook](guidebook/guidebook.md)
and should be considered mandatory reading prior to contributing to this project.

# Prerequisites
* [JDK 8](http://zulu.org/) installed and working
* an SQS queue named `sqs-experiment` -- you can select another name but will have to edit the code

# Building
`./gradlew` will pull down any dependencies, compile the source and package everything up.

# Installation
Nothing to install.

# Tips and Tricks
## Starting The Server
Edit `application.yml`, inserting your API keys.

`./gradlew clean bootRun` will start the server on port `8080` and begin producing messages every second. You should see something similar to this:

```
2017-12-22 10:45:15.560  INFO 32766 --- [enerContainer-4] com.example.sqs.sqs.SqsApplication       : Consuming 10e
2017-12-22 10:45:15.560  INFO 32766 --- [enerContainer-4] com.example.sqs.sqs.SqsApplication       :     LogicalResourceId: sqs-experiment
2017-12-22 10:45:16.105  INFO 32766 --- [enerContainer-4] com.example.sqs.sqs.SqsApplication       : Consuming 110
2017-12-22 10:45:16.105  INFO 32766 --- [enerContainer-4] com.example.sqs.sqs.SqsApplication       :     LogicalResourceId: sqs-experiment
2017-12-22 10:45:16.362  INFO 32766 --- [pool-2-thread-1] com.example.sqs.sqs.SqsApplication       : Producing message 111
2017-12-22 10:45:17.264  INFO 32766 --- [enerContainer-4] com.example.sqs.sqs.SqsApplication       : Consuming 111
2017-12-22 10:45:17.264  INFO 32766 --- [enerContainer-4] com.example.sqs.sqs.SqsApplication       :     LogicalResourceId: sqs-experiment
2017-12-22 10:45:17.363  INFO 32766 --- [pool-2-thread-1] com.example.sqs.sqs.SqsApplication       : Producing message 112
2017-12-22 10:45:18.362  INFO 32766 --- [pool-2-thread-1] com.example.sqs.sqs.SqsApplication       : Producing message 113
2017-12-22 10:45:18.603  INFO 32766 --- [enerContainer-4] com.example.sqs.sqs.SqsApplication       : Consuming 112
2017-12-22 10:45:18.603  INFO 32766 --- [enerContainer-4] com.example.sqs.sqs.SqsApplication       :     LogicalResourceId: sqs-experiment
2017-12-22 10:45:18.865  INFO 32766 --- [enerContainer-4] com.example.sqs.sqs.SqsApplication       : Consuming 113
2017-12-22 10:45:18.865  INFO 32766 --- [enerContainer-4] com.example.sqs.sqs.SqsApplication       :     LogicalResourceId: sqs-experiment
2017-12-22 10:45:19.362  INFO 32766 --- [pool-2-thread-1] com.example.sqs.sqs.SqsApplication       : Producing message 114
2017-12-22 10:45:19.875  INFO 32766 --- [enerContainer-4] com.example.sqs.sqs.SqsApplication       : Consuming 114
2017-12-22 10:45:19.875  INFO 32766 --- [enerContainer-4] com.example.sqs.sqs.SqsApplication       :     LogicalResourceId: sqs-experiment
```


# Troubleshooting

# Contributing

# License and Credits
* This project is licensed under the [Apache License Version 2.0, January 2004](http://www.apache.org/licenses/).
* The guidebook structure was created by [Simon Brown](http://simonbrown.je/) as part of his work on the [C4 Architectural Model](https://c4model.com/).  His books can be [purchased from LeanPub](https://leanpub.com/b/software-architecture).
* Patrick Kua offered [his thoughts on a travel guide to a software system](https://www.safaribooksonline.com/library/view/oreilly-software-architecture/9781491985274/video315451.html) which has been [captured in this template](travel-guide/travel-guide.md).

# List of Changes
