# OcnoAlert - Cancer Detection Machine Learning App

## Description
OcnoAlert is a machine learning application that identifies the type of cancer in medical scan images uploaded by users. The app uses the VGG16 pre-trained model to identify significant features in the images and provides predictions on the type of cancer.

## Technologies Used
- **Python**: Main programming language.
- **Flask**: Web framework for handling file uploads and serving the ML model.
- **OpenCV**: Image processing for resizing and normalization.
- **NumPy**: Numerical computations and data manipulation.
- **Keras**: High-level neural networks API for building the ML model.
- **TensorFlow**: Backend for executing the ML model.
- **Matplotlib**: Plotting library for visualizing model performance.
- **Seaborn**: Statistical data visualization.
- **React**: Front-end framework for building the user interface.
- **Bootstrap**: CSS framework for responsive design.
- **Node.js**: JavaScript runtime for running the React app.

## How to Use

### Installation
1. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
   Ensure all required dependencies are installed before using this program.

### Using Kaggle Dataset
1. **Download the Dataset**:
   - Go to Kaggle and download the desired dataset for cancer detection. For example, you can use the "Breast Cancer Detection" dataset.
   - Extract the downloaded dataset to your project directory.

2. **Prepare Training Data**:
   - Organize the dataset into separate folders under `assets/train`. 
   - Example: `assets/train/breast` should contain pictures of breast cancer.

3. **Prepare Validation Data**:
   - Create identical category folders under `assets/validate` with different images for validation.

### Training the Model
1. **Run the Training Script**:
   ```bash
   python main.py
   ```
   This script trains the model using the data from the `assets/train` folder and provides an accuracy score and confusion matrix.

### Running the Flask Server
1. **Prepare Server Data**:
   - Follow the same process for `assets1/train` as described above.
   - Leave `assets1/validate` empty; uploaded files will go into `assets1/validate/user`.

2. **Create Virtual Environment**:
   ```bash
   python -m venv venv
   ```

3. **Activate Virtual Environment**:
   ```bash
   ./venv/Scripts/activate  # Windows
   source venv/bin/activate  # MacOS/Linux
   ```

4. **Install Dependencies in Virtual Environment**:
   ```bash
   pip install -r requirements.txt
   ```

5. **Run Flask Server**:
   ```bash
   python server.py
   ```

### Running the React App
1. **Navigate to Client Folder**:
   ```bash
   cd client
   ```

2. **Install Client Dependencies**:
   ```bash
   npm install
   ```

3. **Start React App**:
   ```bash
   npm start
   ```

### Using the App
1. **Upload and Analyze**:
   - In the React app, navigate to the test page and upload a file.
   - Click the "UPLOAD" button to upload the file. Check `assets1/validate/user` to ensure the file was uploaded.
   - Click the "ANALYZE" button to see the result. The diagnosis label will update with the predicted result.
   
2. **Cleanup**:
   - Delete the uploaded file in `assets1/validate/user` to run the program again.

## Folder Structure
```
OcnoAlert/
│
├── assets/
│   ├── train/
│   └── validate/
│
├── assets1/
│   ├── train/
│   └── validate/
│       └── user/
│
├── client/
│   ├── node_modules/
│   └── ...
│
├── backend/
│   ├── venv/
│   └── ...
│
├── main.py
├── server.py
├── requirements.txt
├── README.md
└── ...
```

Happy diagnosing with OcnoAlert!
--------------------------------------------------------------
Devpost Link: https://devpost.com/software/oncoalert
