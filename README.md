# Myers-Briggs Personality Prediction based on social media posts

## Problem
I built a machine learning model predicting personality type based on any user provided text. The model is trained on the Kaggle data set (https://www.kaggle.com/datasets/datasnaek/mbti-type) matching results of the MBTI personality test with social media posts. You can run inference swapping
the list of social media posts in the last cell

## Approach
1. EAD. After loading the data set I'm going to thoroughly evaluate it. I'll pay a lot of attention to how balanced the data set is (number of observations per type).
2. Data processing. I assume that I'll have to process the data to clean it up and prepare it for training of a machine learning model.
3. Vectorization. The text data will have to be vectoried to be used by my supervised model.
4. Model training. Based on the aforementioned analysis I'll decide which supervised model, or models, should I use.
5. Model tuning. I'll analyze the performance of the model and try to tune it.
6. Inference. I'm going to write a little inference system and test the final model on an additional data set – my own social media posts.

## Results
Both Logistic Regession and SVM performed relatively well on the data set. SVM had a slight edge and I used it for running inference.

| Trait Pair | LR Accuracy | SVC Accuracy | LR F1-Score | SVC F1-Score |
| :--- | :---: | :---: | :---: | :---: |
| **Thinking (T) vs. Feeling (F)** | **84.67%** | 84.44% | **0.8466** | 0.8449 |
| **Introvert (I) vs. Extravert (E)**| **84.21%** | 84.09% | **0.8455** | 0.8443 |
| **Intuitive (N) vs. Sensing (S)** | 88.36% | **89.74%** | 0.8915 | **0.8873** |
| **Judging (J) vs. Perceiving (P)** | 81.15% | **81.10%** | 0.8118 | **0.8112** |

## How to run the notebook?

### Dependencies
Python 3.8
pandas
numpy
scikit-learn
matplotlib
seaborn
wordcloud

### Data
Unzip the data set mbti-type before running the project

### Cloning repo

```git clone https://https://github.com/marcintreder/mbti-personality-prediction.git```

### About MBTI
MBTI was developed in the 1940s by American Psychologists – Katherine Cook Briggs and Isabel Briggs Meyrs. The test identifies 16 personality types which are grouped by four pairs of opposite preferences:

extraversion (E) or introversion (I),
sensing (S) or intuition (N),
thinking (T) or feeling (F),
and judging (J) or perceiving (P).
Combinations of one letter from each pair results in 16 unique four-letter combinations:

Analysts

INTJ: Architect
INTP: Logician
ENTJ: Commander
ENTP: Debater
Diplomats

INFJ: Advocate
INFP: Mediator
ENFJ: Protagonist
ENFP: Campaigner
Sentinels

ISTJ: Logistician
ISFJ: Defender
ESTJ: Executive
ESFJ: Consul
Explorers

ISTP: Virtuoso
ISFP: Adventurer
ESTP: Entrepreneur
ESFP: Entertainer

Subjects of the MBTI evaluation answer ranking questions such as "At a party do you: a. Interact with many, including strangers, b. Interact with a few known to you". Answers all these questions directly classify subjects into one of the types represented by the opposing pairs of types. Once all four types are established, the four letter meta type becomes evident and it's matched with a predetermined personality description.

Myers-Briggs Type Indicator critique
It's worth noting that while MBTI test continues to be highly popular in the fields of Psychological diagnostics and Psychology of Work and Human Resources, it is widely criticized as a signal of preferences rather than pure indicator of the personality type. One could say that evaluated people choose the vision of themselves that they idealized rather than what is the true expression of their personality.

