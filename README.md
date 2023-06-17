# one-spot_health-Check-up
Importing the required modules and libraries: The code starts by importing the necessary modules and libraries, including Flask, os, joblib, numpy, and Keras.

Setting up the Flask app: The Flask app is created using the Flask class, and the static and template directories are defined.

Defining the routes: Several routes are defined for different sections of the web application, including the home page (/), disease section (/disease), breast cancer section (/breastcancer), diabetes section (/diabetes), heart disease section (/heart), pneumonia prediction section (/pneumonia), and thyroid section (/thyroid).

Breast Cancer Prediction: The /breastcancer route handles the prediction of breast cancer. When a POST request is received with the required form data, the data is extracted, and the breast cancer model is loaded using joblib.load. The model predicts the outcome based on the input data, and the result is rendered in the breastcancer.html template.

Diabetes Prediction: The /diabetes route handles the prediction of diabetes. Similar to the breast cancer prediction, the input data is extracted from the form, the diabetes model is loaded using joblib.load, and the prediction is rendered in the diabetes.html template.

Heart Disease Prediction: The /heart route handles the prediction of heart disease. The input data is extracted from the form, and the heart disease model is loaded using joblib.load. The prediction result is rendered in the heart.html template.

Pneumonia Prediction: The /pneumonia route handles the prediction of pneumonia. When a POST request is received, the uploaded image is saved and passed to the pneumonia_predict function along with the pneumonia model. The function preprocesses the image, makes the prediction, and returns the result. The saved image is then removed from the server, and the prediction is rendered in the pneumonia.html template.

Thyroid Section: The /thyroid route renders the thyroid.html template, which is a static page.

Running the Flask app: The code checks if the script is being run directly and then starts the Flask app on the specified port.
