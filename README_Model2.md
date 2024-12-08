Project Overview
This notebook is designed to process a genetic medical database (GMDB) and build a machine learning model to classify images based on syndromes.

It involves:

Data preparation and filtering.
Image preprocessing and feature extraction.
Training and evaluating a classifier.

Code Overview
 1. Import Dependencies
  Libraries used include:
  Data Manipulation: pandas, numpy
  Image Processing: cv2, MTCNN
  Feature Extraction: DeepFace
  Machine Learning: sklearn
  Visualization: matplotlib, seaborn

2. Dataset Paths and Metadata Loading
 Dataset directories and metadata file paths are defined.
 Metadata is loaded using pandas and filtered for relevant syndrome data.

3. Syndrome Mapping and Data Preparation
 A dictionary maps syndrome names to unique IDs.
 Data is split into training, validation, and testing subsets based on the filtered syndrome IDs.

4. Image Preprocessing
 Face Detection and Alignment:
  Uses the MTCNN library to detect faces in images and crop them for uniformity.
 Feature Extraction:
  Uses DeepFace with the ArcFace model to extract embeddings from aligned face images.

5. Model Training and Evaluation
 Model:
  A Support Vector Classifier (SVC) is trained using extracted embeddings.
 Validation:
  Model is evaluated on validation and test sets for accuracy, classification report, and confusion matrix.

6. Additional Metrics and Visualizations
 Metrics such as precision, recall, F1-score, and top-5 accuracy are calculated.
 Visualizations include:
 Confusion matrix heatmap.
 Bar charts for precision, recall, F1-score by class.
 Macro average metrics.


Instructions to Use
 Dependencies Installation:
 Ensure the following libraries are installed: pandas, numpy, opencv-python, mtcnn, deepface, sklearn, matplotlib, seaborn.

File Organization:
 Place the dataset folders (gmdb_crops, gmdb_images, gmdb_metadata) in the specified directory structure.

Run the Notebook:
 Execute cells sequentially to preprocess data, train the model, and evaluate its performance.

Output:
 Model evaluation metrics will be printed.
 Visualization plots for metrics and confusion matrix will be displayed.


Key Outputs
 Validation Accuracy
 Test Accuracy
 Confusion Matrix
 Classification Report
 Visualization of Performance Metrics


Notes
  Ensure all file paths are updated correctly based on your local setup.
  Images without detectable faces or feature extraction failures are logged but skipped.
  The model is trained on ArcFace embeddings, which might need fine-tuning for different datasets or syndrome categories.
