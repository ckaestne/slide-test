---
author: Christian Kaestner
title: Data and Model Quality (QA for ML)
date: Spring 2019
footer: '17-445 Software Engineering for AI-Enabled Systems, Christian Kaestner'
theme: 'white'
---  


# Data and Model Quality (QA for ML)

Christian Kaestner


<a href="..">test</a>

----

# Math

$f(x)=x_i+1$
----

# mermaid





```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

----

# Notes

test

Note:

foo

bar
c

----

# 2 columns


some text

more text

<!-- split -->
![](course_overview.png)


----

<!-- colstart -->
# nested columns



c 1 Content
<!-- col -->
# right
<!-- colstart -->
inner
<!-- col -->
inner 2
<!-- colend -->
<!-- colend -->


----

<!-- small -->
# Full slide in smaller font

- a
- b
- b
- b
- b
- b
- b
- b

----

# <!-- fit --> Long title that is made to fit on a slide without breaking

using the fit comment

----

## And a table
<!-- small -->

| RestaurantID | Order| OrderTime|ReadyTime|PickupTime|
|-|-|-|-|-|
| 5 |5A;3;10;11C;C:No onion| 18:11|18:23|18:31|
|...|
|...|
|...|


---

![](course_overview.png)





---

<!-- small --> 
# Learning Goals

* Understand the challenges of testing AI components of a system

* Understand the basic steps of a machine learning pipeline

* Apply measures of model quality

* Select mechanisms to assure data quality in production, e.g., detect drift

* Describe opportunities for QA automation in a machine learning pipeline

* Apply basic tests for sensitivity, fairness




---

<!-- small -->

# <!-- fit --> Fall 2019: New Course: Software Engineering for AI-Enabled Systems


<!-- colstart -->
https://ckaestne.github.io/seai/
* What changes with AI? Requirements, Architecture, Operations, Quality assurance, Process
* Going beyond Jupyter notebooks, operating AI-enabled systems in practice at scale
* Software engineering view on AI/ML craze

<!-- col -->

![bg right  fit](image2.png)
<!-- colend -->

<!-- /small -->

---

# Case Study



---

# Order?


![bg](image3.png)


---

## Predicting Delivery Times

What factors may it depend on?

What can be used for learning and prediction?

How to evaluate accuracy?

One model or multiple?



---




# Machine Learning Pipeline


----





## Typical ML Pipeline

- Static
  - Get labeled data
  - Identify and extract features
  - Split data into training and evaluation set
  - Learn model from training data
  - Evaluate model on evaluation data
  - Repeat, revising features

- With production data
  - Evaluate model on production data; monitor
  - Select production data for retraining
  - Update model regularly


----

<!-- small -->



## Example Data

| RestaurantID | Order| OrderTime|ReadyTime|PickupTime|
|-|-|-|-|-|
| 5 |5A;3;10;11C;C:No onion| 18:11|18:23|18:31|
|...|
|...|
|...|

