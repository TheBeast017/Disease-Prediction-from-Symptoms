# Disease Prediction from Symptoms

This project explores the use of machine learning algorithms to predict diseases from symptoms. The system leverages different algorithms to predict diseases based on a set of symptoms.

### Algorithms Explored

The following algorithms have been implemented and tested in the project:

1. **Naive Bayes**
2. **Decision Tree**
3. **Random Forest**
4. **Gradient Boosting**

### Dataset

The dataset used in this project consists of symptoms and the corresponding disease (prognosis). The training and test datasets come from different sources:

#### Source 1 (Kaggle Dataset)

The dataset used with the `main.py` script is downloaded from the Kaggle repository:

https://www.kaggle.com/kaushil268/disease-prediction-using-machine-learning


This dataset contains 133 columns:
- 132 columns represent various symptoms experienced by the patients.
- 1 column represents the disease prognosis for the corresponding symptoms.

#### Source 2 (Columbia Dataset)

This dataset is used with the Jupyter Notebook for training models and inference. It is available from:

https://impact.dbmi.columbia.edu/~friedma/Projects/DiseaseSymptomKB/index.html

markdown
Copy code


This dataset contains 3 columns:
- **Disease**
- **Count of Disease Occurrence**
- **Symptom**

You can either copy-paste the table into an Excel sheet or scrape it using BeautifulSoup.

### Directory Structure

|_ dataset/ |_ training_data.csv # Training dataset |_ test_data.csv # Test dataset

|_ saved_model/ |_ [pre-trained models] # Saved models (Decision Tree, Random Forest, Gradient Boosting, etc.)

|_ main.py # Code for loading Kaggle dataset, training, and saving models

|_ infer.py # Code for inference on custom symptoms

|_ demo.py # Code for interactive demo using Gradio

|_ notebook/ |_ dataset/ |_ raw_data.xlsx # Columbia dataset for Jupyter notebook |_ Disease-Prediction-from-Symptoms-checkpoint.ipynb # Jupyter notebook for loading the Columbia dataset, training the model, and making predictions


### Installation

Please install all dependencies before running the demo by using the following:

pip install -r requirements.txt


### Usage

#### 1. **Running `main.py` (Training the Models)**

To train the models, run the `main.py` script, which loads the training dataset, trains different machine learning models, and saves them for future use.

python main.py


#### 2. **Running `infer.py` (Inference on Custom Input)**

You can use the `infer.py` script to make predictions for new symptoms. It requires symptoms as a comma-separated string passed as an argument:

python infer.py "itching, skin_rash, fever"


This will output the predicted disease based on the symptoms.

#### 3. **Interactive Demo using `demo.py`**

For an interactive web-based demo, you can use Gradio. The `demo.py` script allows users to select symptoms via a graphical interface and get predictions.

To run the interactive demo:

python demo.py


This will launch a Gradio interface where you can input symptoms and get predictions in real time.

### Model Details

The models trained in this project include:
- **Decision Tree Classifier** with `entropy` criterion
- **Random Forest Classifier** with 10 estimators
- **Gradient Boosting Classifier** with 150 estimators and `friedman_mse` criterion
- **Naive Bayes Classifier**

The models are trained and saved to the `saved_model/` directory.

### Notes

- This project is designed for educational and demo purposes. For any health-related concerns or symptoms, please consult with a medical professional.
- The `infer.py` script and Gradio demo can be used to test the models on new symptom inputs.
- The system is built to predict the most likely disease based on the symptoms provided.

### License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.
