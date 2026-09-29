# Project Statement

## 1. Problem Statement

Crop diseases can negatively affect plant growth, crop quality, and
agricultural productivity. Identifying a disease from visible symptoms
can be difficult, particularly when different diseases have similar
symptoms.

The **Crop Disease Prediction System** addresses this problem by
providing a simple symptom-based system in which a user selects a crop
and enters the symptoms observed on the plant. The system compares the
selected symptoms with a predefined knowledge base of crop diseases and
identifies the disease with the highest similarity.

The system also provides the predicted disease's confidence score,
severity level, treatment recommendation, and prevention information.

## 2. Scope of the Project

The scope of the project includes the development of a console based
crop disease prediction application using Python and NumPy.

The current system covers:

-   Four crops:
    -   Tomato
    -   Wheat
    -   Potato
    -   Rice
-   A predefined symptom library for each supported crop.
-   A predefined disease knowledge base.
-   Multiple symptoms as user input.
-   Binary vector representation of symptoms.
-   Cosine similarity-based disease matching.
-   Ranking of diseases according to similarity.
-   Prediction confidence display.
-   Disease severity information.
-   Treatment recommendations.
-   Prevention recommendations.
-   Session-based prediction history.
-   Input validation for crop selection and symptom codes.

The current project does **not** include image-based disease detection,
deep-learning image classification, real-time sensor data, or a
web/mobile user interface.

## 3. Target Users

The system is intended for users who need a simple way to explore
possible crop diseases from observed symptoms, including:

-   Farmers
-   Agriculture students
-   Students learning about artificial intelligence or machine learning
    concepts
-   Agriculture related learners and educators
-   Users interested in basic crop disease identification

The system is designed as an educational and decision support project.
It is not intended to replace professional agricultural diagnosis.

## 4. High-Level Features

### 4.1 Crop Selection

Users can select one of the supported crops: Tomato, Wheat, Potato, or
Rice.

### 4.2 Symptom Selection

The system displays the symptoms available for the selected crop and
allows users to select all symptoms that apply using symptom codes.

### 4.3 Disease Prediction

The system converts the observed symptoms and disease symptoms into
binary vectors and calculates cosine similarity to determine how closely
they match.

### 4.4 Ranked Disease Results

Diseases are ranked by their similarity score, allowing the system to
identify the highest-scoring disease and, when applicable, display
another possible match.

### 4.5 Prediction Report

The prediction report includes:

-   Crop name
-   Predicted disease
-   Confidence score
-   Severity level
-   Recommended treatment
-   Prevention advice

### 4.6 Severity Classification

Each disease in the knowledge base is associated with a severity level:

-   High
-   Medium
-   Low

The system converts these levels into corresponding warning labels for
the displayed report.

### 4.7 Recommendation System

For each supported disease, the project stores predefined treatment and
prevention information and displays the relevant information after
prediction.

### 4.8 Prediction History

The system records predictions made during the current session and
displays them in a session summary when the program ends.

### 4.9 Input Validation

The system validates crop selection and handles invalid or unrecognised
symptom codes. It also handles cases where the user selects no symptoms.


