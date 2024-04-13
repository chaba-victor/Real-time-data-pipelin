<div align="center">
    <h1>Building a production-ready feature pipeline is real-time</h1>

    
</div>

## Tools

- Apache Kafka
- Python
- [Quix Streamx](https://github.com/quixio/quix-streams)


#### Table of contents
* [Aim](#Aim)
* [Pipelines](#Pipelines)
    - Injestion
    - Transformation
    - Saving to a feature store
* [Running the pipeline natively](#running-the-pipeline-natively)
* [Deployment](#deployment)
* [Dashboard for monitoring](#Dashboard-for-monitoring)
* [Wanna learn more about ML?](#Wanna-learn-more-about-ML?)


## Aim

The ultimate goal is to build a trading boat that is powered by ML.

Before even thinking about how the ML model will do its thing, we'll need to design, develop and deploy a **real-time feature pipeline** that produces the features needed by the model both at training and at inference.


The pipeline has 3 parts:

- **Ingestion** of raw data from an external service. This would be raw trades. Kraken Websocket API will do.

- **Transform** these trades into features for the ML model.

- **Saving** these features in a Feature Store, to be fetched by the ML modelto generate both the training data and real-time predictions.

In a real-world setting, each of the above processes is implemented as a separate service, and communication between these services happens through a message broker like Kafka.


This way, yoursystem becomes scalable by spinning up more containers as needed, and leveraging Kafka consumer groups.




## Wanna learn more about ML?

[→ Take a look 🤗](https://www.cicada.blog)
