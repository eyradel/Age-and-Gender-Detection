
# Age and Gender Detection App

This is a web application that uses OpenCV and deep learning models to detect age and gender from an uploaded or captured image. The app is built using Streamlit for the frontend and OpenCV for image processing.

## Features
- Detects human faces from an image.
- Predicts the gender (Male/Female) of detected faces.
- Predicts the approximate age group of detected faces.
- Allows users to either upload an image or capture one using their camera.

## Tech Stack
- **Frontend:** [Streamlit](https://streamlit.io/)
- **Backend:** [OpenCV](https://opencv.org/), [DNN Models](https://github.com/spmallick/learnopencv)
- **Languages:** Python

## Models Used
- **Face Detection Model:** OpenCV DNN based face detector.
- **Age Detection Model:** Pre-trained deep learning model using Caffe.
- **Gender Detection Model:** Pre-trained deep learning model using Caffe.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/age-gender-detection-app.git
   cd age-gender-detection-app
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Download the necessary models and place them in the `models` folder. You can download the pre-trained models from the following links:
   - [Face Detection Model](https://github.com/spmallick/learnopencv/blob/master/FaceDetectionComparison/models/opencv_face_detector_uint8.pb)
   - [Age Detection Model](https://github.com/spmallick/learnopencv/blob/master/AgeGender/models/age_net.caffemodel)
   - [Gender Detection Model](https://github.com/spmallick/learnopencv/blob/master/AgeGender/models/gender_net.caffemodel)

4. Run the application:

   ```bash
   streamlit run app.py
   ```

## Usage

1. Choose either "Upload Image" to upload a local image or "Capture Image" to take a photo using your webcam.
2. The app will process the image and display the detected faces, along with predictions for the age and gender of each face.
3. The detection results are shown on the right side, highlighting the predicted age group and gender.

## Folder Structure
```plaintext
.
├── app.py                  # Main app file
├── models                  # Folder containing the pre-trained models
│   ├── opencv_face_detector.pbtxt
│   ├── opencv_face_detector_uint8.pb
│   ├── age_deploy.prototxt
│   ├── age_net.caffemodel
│   ├── gender_deploy.prototxt
│   ├── gender_net.caffemodel
├── requirements.txt        # Required Python libraries
└── README.md               # This readme file
```

## Requirements
- Python 3.8+
- Streamlit
- OpenCV
- Numpy
- Pillow (PIL)

Install dependencies via:

```bash
pip install -r requirements.txt
```

## Known Issues
- The app might not detect faces properly in low-resolution or blurry images.
- Make sure the image contains visible human faces for accurate detection.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
- Pre-trained models for age and gender detection are taken from [LearnOpenCV](https://learnopencv.com/age-gender-classification-using-opencv-deep-learning-c-python/).
- Special thanks to the contributors of OpenCV and Streamlit for their amazing work!
