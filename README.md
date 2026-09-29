# Crop Disease Prediction System

## 1. Project Title ---------------------------------------------------------

**Crop Diseases Prediction System**

## 2. Overview of the Project -----------------------------------------------

The Crop Disease Prediction System is a Python based application that
predicts the most likely disease affecting a selected crop from the
symptoms entered by the user.

The system uses a predefined knowledge base containing crop symptoms,
diseases, disease severity, treatment recommendations, and prevention
information. The prediction engine converts the selected symptoms into
binary vectors and compares them with the symptom vectors associated
with each known disease using **cosine similarity**.

The system currently supports four crops:

-   Tomato
-   Wheat
-   Potato
-   Rice

After prediction, the system displays the predicted disease, confidence
score, severity level, recommended treatment, and prevention advice. It
also keeps a prediction history during the current program session.

**Note:** This project is a symptom-based prediction system. It does
          not use image processing, deep learning, or a trained
          image-classification model.

## 3. Features -------------------------------------------------------------

-   Select a crop from the supported crop list.
-   View the symptom library for the selected crop.
-   Select multiple observed symptoms using symptom codes such as s1,
    s3, and s5.
-   Compare observed symptoms with the known disease symptoms.
-   Calculate disease similarity using cosine similarity.
-   Rank diseases according to their similarity score.
-   Display the top predicted disease.
-   Display a confidence score for the prediction.
-   Show disease severity as **High**, **Medium**, or **Low**.
-   Provide recommended treatment information.
-   Provide prevention advice for the next season.
-   Display another possible disease match when available.
-   Maintain prediction history during the current session.
-   Handle invalid crop choices and unrecognised symptom codes.
-   Provide a message when no symptoms are selected or no close match is
    found.
-   Demonstrate object oriented programming concepts including
    inheritance and polymorphism.

## 4. Technologies / Tools Used -------------------------------------------

### Programming Language

-   **Python 3**

### Python Library

-   **NumPy** -- used to create symptom vectors and perform numerical
    calculations, including dot products and vector norms for cosine
    similarity.

### Development Environment

The uploaded project is provided as a **Jupyter Notebook (`.ipynb`)**.
It can be executed in:

-   Jupyter Notebook
-   JupyterLab
-   Google Colab
-   Another Python environment that supports Jupyter notebooks

### Main Technical Concepts

-   Knowledge-base approach
-   Binary symptom vectors
-   Cosine similarity
-   Object-oriented programming (OOP)
-   Inheritance
-   Polymorphism
-   Session-based prediction history
-   Console-based user interaction

## 5. Steps to Install & Run the Project ----------------------------------

1. Install Python 3
2. Install NumPy:
   ```bash
   pip install numpy
   ```
3. Open `Crop Diseases Prediction System.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab
4. Run the notebook cells
5. Select a crop and enter the observed symptoms
6. View the predicted disease and recommendation

## 6. Instructions for Testing---------------------------------------------

Testing can be performed by running the notebook and checking different
input scenarios.

### Test Case 1: Tomato Disease Prediction

1.  Run the program.
2.  Select `1` for Tomato.
3.  Enter:

``` text
s1,s2,s6
```

4.  Verify that the system produces a prediction report and displays a
    confidence score, severity, treatment, and prevention information.

### Test Case 2: Wheat Disease Prediction

1.  Select Wheat.
2.  Enter:

``` text
s1,s2,s5
```

3.  Verify that a Wheat disease is predicted and the corresponding
    recommendation is displayed.

### Test Case 3: Potato Disease Prediction

1.  Select Potato.
2.  Enter:

``` text
s1,s2,s5
```

3.  Verify that the system produces a prediction and displays the
    disease information.

### Test Case 4: Rice Disease Prediction

1.  Select Rice.
2.  Enter:

``` text
s1,s3
```

3.  Verify that the system displays a Rice disease prediction and its
    recommendation.

### Test Case 5: Invalid Crop Input

At the crop selection screen, enter an invalid value such as:

``` text
10
```

Verify that the program displays a message indicating that the choice is
out of range.

Also test a non-numeric input such as:

``` text
abc
```

The program should ask for a valid number.

### Test Case 6: Invalid Symptom Code

For a selected crop, enter a mixture of valid and invalid codes, for
example:

``` text
s1,s3,s99
```

Verify that the recognised symptoms are used and the unrecognised code
is reported and ignored.

### Test Case 7: No Symptoms Selected

At the symptom input prompt, submit an empty input.

Verify that the system displays:

``` text
No symptoms selected -- skipping prediction.
```

and does not attempt to generate a disease prediction.

### Test Case 8: No Close Match

Enter a symptom combination that produces zero similarity for the
available diseases.

Verify that the program displays a message indicating that no close
match was found and suggests trying more or different symptoms.

### Test Case 9: Prediction History

Make multiple valid predictions during one session.

Exit the program and verify that the session summary contains the crop,
predicted disease, and confidence for predictions recorded during that
session.

## 7. Expected Result ---------------------------------------------------------

The expected result is a console-based crop disease prediction system
that accepts a crop and observed symptoms, compares those symptoms with
the predefined disease knowledge base, and provides a ranked prediction
together with confidence, severity, treatment, and prevention
information.

## 8. Important Limitation-----------------------------------------------------

The current implementation is based on a manually defined symptom and
disease knowledge base. Its prediction score represents **cosine
similarity between symptom vectors**, rather than a probability learned
from a machine-learning training dataset.

The treatment and prevention information displayed by the application is
part of the project's predefined knowledge base and should be treated as
project guidance rather than a substitute for professional agricultural
diagnosis.
