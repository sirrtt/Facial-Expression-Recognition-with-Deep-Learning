# Facial Expression Recognition Application

This project is a web application for real-time facial expression recognition using different machine learning models. The application is built using Streamlit and deployed using Docker.

## Demo

### Real-time demo
https://github.com/user-attachments/assets/3630185b-c1f3-47bf-9c00-886292a4c1b9

### Application demo
https://github.com/user-attachments/assets/59294091-ecab-4fe6-82cc-7cddfd801b23

## Project Structure

```

Facial-Expression-Recognition
│
├── Application
│   ├── app.py
│   ├── haarcascade_frontalface_default.xml
│   ├── Dockerfile
│   ├── requirements.txt
│   └── docker-compose.yml (optional)
│
├── Code
│   ├── CNN_from_scratch_method
│   │   ├── CNN_from_scratch.ipynb
│   │   └── model
│   │       ├── best_face_model.json
│   │       └── best_model.h5
│   │
│   ├── DeepFace_method
│   │   └── DeepFace.ipynb
│   │
│   ├── Demo_CNN_method
│   │   └── CNN_demo_real_time.py
│   │
│   ├── Demo_DeepFace_method
│   │   └── DeepFace_demo_real_time.py
│   │
│   └── SVM_method
│       ├── model
│       │   └── svm_emotion_model.joblib
│       └── SVM.ipynb
│
├── Dataset
└── Reports

```

## Features

- Real-time facial expression recognition using CNN, DeepFace, and SVM models.
- Visualization of detected faces with bounding boxes and predicted emotions.
- User-friendly interface built with Streamlit.
- Dockerized for easy deployment.

## Getting Started

### Prerequisites

- Python 3.8.19
- Docker
- Docker Compose (optional)

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/Facial-Expression-Recognition.git
   cd Facial-Expression-Recognition/Application
   ```

2. Ensure you have a `requirements.txt` file in the `Application` directory with the dependencies listed above.

   ```bash
   pip install -r requirements.txt
   ```

### Usage

#### 1. Running the Application Locally

You can run the application locally using Streamlit.

```bash
streamlit run app.py
```

Open your web browser and navigate to `http://localhost:8501` to see the application.

#### 2. Running the Docker Container

If you prefer to use Docker, you can pull and run the Docker image directly from Docker Hub.

   1. **Pulling the Docker Image**
   
      To pull the Docker image from Docker Hub, use the following command:
      
      ```bash
      docker pull percevalwilhelm/emotion-detection-app
      ```
   
   2. **Running the Docker Container**
   
      Run the Docker container using:
      
      ```bash
      docker run -p 8501:8501 percevalwilhelm/emotion-detection-app
      ```
   
      You can now access the application in your web browser at `http://localhost:8501`.

#### 3. Using Docker

   1. **Build the Docker Image:**
   
      ```bash
      docker build -t emotion-detection-app .
      ```
   
   2. **Run the Docker Container:**
   
      ```bash
      docker run -p 8501:8501 emotion-detection-app
      ```
   
   3. Open your web browser and navigate to `http://localhost:8501` to access the application.

#### 4. Using Docker Compose (Optional)

   1. Create a `docker-compose.yml` file in the `Application` directory with the following content:
   
      ```yaml
      version: '3'
      services:
        app:
          build: .
          ports:
            - "8501:8501"
      ```
   
   2. **Run Docker Compose:**
   
      ```bash
      docker-compose up
      ```
   
   3. Open your web browser and navigate to `http://localhost:8501` to access the application.

### File Details

#### `app.py`

The main application script for Streamlit. It includes functions to load models, process images, predict emotions, and display results.

#### `Dockerfile`

Defines the Docker image configuration for the application.

#### `requirements.txt`

Lists all the Python dependencies required for the application.

#### `docker-compose.yml` (Optional)

Defines the Docker Compose configuration for the application.

### Model Files

- **CNN Model:**
  - `Code/CNN_from_scratch_method/model/best_face_model.json`
  - `Code/CNN_from_scratch_method/model/best_model.h5`

- **SVM Model:**
  - `Code/SVM_method/model/svm_emotion_model.joblib`

## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Special thanks to the contributors of the DeepFace and Streamlit libraries.
- Thanks to all the open-source contributors and the community for their support.
