# ClickVision
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Apache Spark](https://img.shields.io/badge/Apache%20Spark-FDEE21?style=flat-square&logo=apachespark&logoColor=black)
![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white)


Event Prediction using Clickstream data using Partially-observable markov chains and Transition Matrices. 

----
A Personalised Sequential Decision Making Framework developed for predicting the Depositing Behaviour of the user.

### Why?

Any startup/company would want to know which user would give a positive ROI, and detecting this early on in the user lifecycle is crucial. This leads to minimising losses and rewarding desired behaviour from the user. Here we face the problem of finding the users who will deposit within the 5 mins of their signing-up on the platform.

### What did we do?

We created a sequential decision predicting and temporal agnostic algorithm which predicts whether the person will make a deposit or not. This method uses the concepts from Traditional Reinforcement Learning but does not utilize the agent and reward paradigm. But focuses majorly on the Markov Decision Processes

### How?

We studied the concepts of Reinforcement Learning and Probabilistic Decision Making to come with this approach. This model takes in clickstream data of the selected user (sign-up/ existing) and further predicts the future steps one by one while fetching values from the Transition Matrices created while training the model on the data.

Technologies uesd are: Python, Pyspark, Parquet, 