# FakeVision — AI-Powered Deepfake Detection System

FakeVision is an AI-powered web application designed to identify potential deepfake manipulation in images and videos. It combines a modern React frontend with a Python Flask backend to provide an accessible interface for submitting media, running detection models, and viewing prediction results.

The project explores deepfake detection through spatial image analysis and temporal video analysis, helping users assess whether uploaded media may contain AI-generated or manipulated content.

## Overview

The rapid advancement of generative AI has made synthetic images and videos increasingly realistic. FakeVision provides a convenient way to analyze suspicious media using deep learning-based detection models.

Users can upload images or videos through the web interface and receive prediction results with confidence scores and visual indicators.

## Key Features

- **Image Deepfake Detection:** Analyze uploaded images for visual patterns associated with deepfake manipulation.
- **Video Deepfake Detection:** Evaluate video content for spatial artifacts and temporal inconsistencies.
- **Confidence Scores:** Present model prediction confidence to help users interpret detection results.
- **Interactive Results:** Display detection outcomes through clear visual indicators.
- **Modern User Interface:** React-based dashboard with a high-tech design and dark mode support.
- **Frontend–Backend Integration:** Communicate with the Flask API to process uploaded media and return results.
- **Modular Architecture:** Keep the user interface and detection API separate for easier maintenance and further development.

## Technology Stack

| Component | Technology |
|---|---|
| Frontend | React |
| Frontend tooling | Vite |
| Backend API | Python, Flask |
| AI/ML | Deep learning-based image and video analysis |
| API communication | HTTP requests between frontend and backend |

## Project Structure

The repository contains the frontend application in the root directory and the backend API in a separate folder.

```text
FakeVision/
├── src/                           # React application source
├── public/                        # Static frontend assets
├── deepfake-detection-api-main/   # Flask backend API
│   ├── app.py                     # API entry point
│   └── requirements.txt           # Python dependencies
├── package.json                   # Frontend dependencies and scripts
├── index.html                     # Frontend entry HTML
└── README.md                      # Project documentation
```

*Note: The structure above illustrates the main components. Actual filenames and folders may differ depending on the repository contents.*

## How It Works

### 1. Media Upload

Users select an image or video through the web interface. The frontend prepares the media for submission to the backend API.

### 2. Backend Processing

The Flask API receives the uploaded media and routes it through the relevant detection pipeline.

### 3. Deepfake Analysis

- **Image pipeline:** Examines visual features that may indicate manipulation or AI generation.
- **Video pipeline:** Analyzes video frames and, where supported by the model, temporal information across frames.

### 4. Result Generation

The backend returns the model's prediction and associated confidence information, which the frontend displays in an accessible format.

**Important:** Detection results are model predictions, not definitive proof that media is authentic or manipulated.

## Getting Started

### Prerequisites

Install the following before running the project:

- Node.js and npm
- Python 3.8 or a compatible version supported by the backend dependencies
- Git
- A compatible Python environment for the model and its dependencies

### 1. Clone the Repository

```bash
git clone <repository-url>
cd FakeVision
```

Replace `<repository-url>` with the URL of your GitHub repository.

### 2. Configure the Frontend

From the project root directory, install the Node.js dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Vite will display the local URL where the frontend is available, typically `http://localhost:5173`.

### 3. Configure the Backend

Open a separate terminal and navigate to the backend directory:

```bash
cd deepfake-detection-api-main
```

Create and activate a virtual environment.

**Windows:**

```bash
python -m venv venv
venv\Scripts\activate
```

**Linux/macOS:**

```bash
python3 -m venv venv
source venv/bin/activate
```

Install the backend dependencies:

```bash
pip install -r requirements.txt
```

Start the Flask application:

```bash
python app.py
```

Use the host and port configured by the backend application when connecting the frontend.

### 4. Connect the Frontend and Backend

Ensure the frontend sends requests to the correct Flask API address. If the API URL is configurable through environment variables, use the variable name expected by the application and configure it for your local environment.

Both services must be running for the complete application workflow to function.

## Usage

1. Open FakeVision in your browser.
2. Select the image or video detection feature.
3. Upload the media you want to analyze.
4. Start the detection process.
5. Review the prediction, confidence score, and displayed result.
6. Repeat the process with other media as needed.

For best results, use media formats and file sizes supported by the backend. Detection accuracy may vary with compression, image quality, video length, and the types of manipulation used.

## Potential Applications

FakeVision can serve as a demonstration and research platform for:

- Exploring deepfake detection techniques.
- Studying AI-generated and manipulated media.
- Demonstrating image and video classification workflows.
- Understanding how machine learning models can be integrated into web applications.
- Experimenting with user-facing AI inference systems.

## Limitations

- Model predictions may include false positives and false negatives.
- Confidence scores should not be interpreted as guaranteed probabilities of authenticity.
- Performance depends on the models, datasets, and preprocessing methods used.
- New generative techniques may produce media that existing detection models fail to identify.
- The application should be treated as an assistive analysis tool, not a definitive forensic verification system.

## Future Improvements

Potential areas for further development include:

- Expanding evaluation across newer deepfake datasets.
- Improving robustness against compression and unseen manipulation techniques.
- Adding automated testing and more detailed error handling.
- Optimizing inference latency and resource utilization.
- Improving deployment configuration, monitoring, and scalability.
- Providing clearer explanations of model predictions where supported.

## License

This project is licensed under the MIT License. See the `LICENSE` file for the full license text.

## Acknowledgements

FakeVision was developed as an exploration of deepfake detection, deep learning, and full-stack AI application development. It demonstrates the integration of machine learning inference with a web-based user experience.
