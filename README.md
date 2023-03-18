# Syntactic_Processing_BeHealthy
A health tech company called **‘BeHealthy’**. They aim to connect the medical communities with millions of patients across the country. 
BeHealthy has a web platform that allows doctors to list their services and manage patient interactions and provides services for patients such as booking interactions with doctors and ordering medicines online. Here, doctors can easily organise appointments, track past medical records and provide e-prescriptions.

### Problem Statement
**BeHealthy** require <font color = 'blue'>**predictive model**</font> which can <font color = 'green'>**identify disease and treatment**</font> from the patients interaction with doctor or ordering medicines online.

### Observation
- Here, idea is to extract the **useful information** from text and in addition to that the **entity of the useful information** also need to be identified. 
- Because the information we are planning to extract from the statement/interactions between doctor and patients are related to medical terms which are not regular usage day-to-day words.

- By observing the requirement, it is clearly visible that we have to process the textual sentence and identify the entities like **Disease and Treatment**. We can predict these all requirements using 
        -  CRF (Conditional Random Field) classifier
        -  Random Forest Classifier
        -  HMM (Hidden Markov Model)

### Approach
#### Model Explanation
1. For Medical Entity Recognition, we are building CRF model which uses custom NER becuase the entities we are planning to recognise all are related to medical terminologies.
2. Luckily!! we received dataset which contains sentences along with labels, labels/tags are very important for Entity recognition. *If your dataset is not labelled, you have to manually label the data for Model Building and Prediction*.

#### Dataset Explanation
We have four data file for this activity to proceed, they are
1. Train Sentence Dataset
2. Train Label Dataset
3. Test Sentence Dataset
4. Test Label Dataset

Developed by [@rajagopal-dandamudi]

Sentence file contains all interations between patients and doctor and Label file contains all enitiy tags for particular words arranged as per sentence. We need to do few preprocessing while accessing dataset we will explore that in further steps

#### Library Explanation
1. Pandas - Dataframe, Content storage and processing
2. Regular Expression (re) - Identify the textual pattern
3. SpaCy - NLP, POS tag check
4. Warnings - To avoid warning messages
5. Sklearn_CRFsuite - Model building and Evaluation
