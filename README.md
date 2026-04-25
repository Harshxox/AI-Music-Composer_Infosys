## AI-Based Music Composition System
An end-to-end AI-powered system that generates unique instrumental music tracks from simple text prompts and also supports audio genre classification.

Built as part of Infosys Springboard Virtual Internship 6.0, this project combines AI, Machine Learning, and Full-Stack Development to automate music creation.

## Project Overview
This system allows users to:
### 1.🎵 Generate music using text prompts (via MusicGen)
### 2. 🎧 Classify uploaded audio into genres (using YAMNet)
### 3. 📚 Store and manage generated tracks
### 4. ⚡ Experience real-time AI-powered music creation
## Key Features

1. **AI Music Generation**: Creates custom instrumental music from text prompts using MusicGen AI model
2. **Text-to-Music**: Converts descriptive text prompts (e.g., "happy energetic pop music") into actual music tracks
3. **Audio Genre Classification**: Classifies music files into 10 different genres using TensorFlow/Keras
4. **Professional UI**: Modern, responsive web interface with dark mode and gradient animations
5. **Complete Full-Stack System**: Works together with backend Flask API and frontend React app

## Technologies Used

- **Frontend**: React.js, HTML5, CSS3
- **Backend**: Python, Flask  (Genre Classification API), FastAPI (Music Generation API)
- **AI Models**: Facebook MusicGen (HuggingFace), TensorFlow/Keras, YAMNet(Audio Classification)
- **Libraries**: PyTorch, TensorFlow, librosa, transformers, audiocraft
- **Deployment**: Local development environment

## Repository Structure

```
AI-Music-Generation-System_Infosys/
│
├── assets/ # UI images, icons, and frontend assets
│
├── backend/ # Backend (Flask - Genre Classification)
│ ├── models/ # Trained ML models
│ │ └── yamnet_gtzan... # Saved YAMNet + GTZAN classifier model
│ │
│ ├── app.py # Flask API for genre classification
│ ├── extract_embeddings.py # Feature extraction using YAMNet
│ ├── gtzan.py # Genre prediction logic
│ └── train_classifier.py # Model training script
│
├── data/ # Dataset & processed features
│ ├── gtzan/ # GTZAN dataset (audio files)
│ ├── images_original/ # Dataset images (if used)
│ ├── features_3_sec.csv # Extracted features (3 sec clips)
│ ├── features_30_sec.csv # Extracted features (30 sec clips)
│ └── gtzan_embeddings... # Precomputed embeddings
│
├── musicgen_model.py # Music generation logic (MusicGen)
├── server.py # FastAPI server for music generation
│
├── index.html # Main frontend UI (music generation)
├── home.html # Landing / login page
│
├── .gitignore # Git ignore file
├── README.md # Project documentation
│
└── venv/ # Virtual environment (ignored)
```

## Project Screenshots
![alt text](image.png)
### 1.Login Page
![alt text](image.png)
### 2.Music Generation UI


Follow these steps to run the project locally:

### Prerequisites

- Python 3.8+
- Node.js 16+
- npm

### 1. Backend Setup

```bash
# Navigate to backend directory
cd backend

# Create virtual environment (optional but recommended)
python -m venv venv

# Activate virtual environment
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run the Flask server
python app.py
```

The backend API will start at: http://localhost:5000

### 2. Frontend Setup

```bash
# Navigate to frontend directory
cd frontend

# Install dependencies
npm install

# Start the development server
npm start
```

The frontend application will start at: http://localhost:3000

## How to Use

### Music Generation

1. Open http://localhost:3000 in your browser
2. Go to the "Music Composer" tab
3. Enter a text prompt describing the music you want (e.g., "calm relaxing piano music for study", "upbeat energetic electronic dance track", "epic orchestral cinematic music")
4. Click "Generate Music"
5. Wait for the AI to process your request (this may take 30-60 seconds depending on your system)
6. Once generated, the track will appear in the list below with playback controls

### Audio Classification

1. Go to the "Genre Classifier" tab
2. Click "Choose File" and select an audio file (MP3, WAV, FLAC, etc.)
3. Click "Classify Genre"
4. The system will analyze the audio and display the predicted genre with confidence level

## Project Status

- ✅ **Backend API**: Functional with MusicGen integration
- ✅ **Frontend UI**: Complete with all features
- ✅ **Genre Classifier**: Working with TensorFlow/Keras
- ✅ **Full Integration**: Backend and frontend connected
- ✅ **User Authentication**: Email/password registration and login
- ✅ **Responsive Design**: Works on desktop and mobile

## Next Steps (Optional Enhancements)

1. Add more advanced AI models (e.g., MusicGen 2, Riffusion)
2. Implement streaming audio playback for long tracks
3. Add user accounts and music library management
4. Deploy to cloud platforms (Heroku, AWS, or Azure)
5. Add BPM and key detection
6. Implement music visualization effects
7. Create a mobile app version using React Native

## Important Notes

- **Model Downloads**: The MusicGen model will be downloaded automatically on first run (large file, ~2GB)
- **Performance**: Music generation requires significant CPU/GPU resources. On slower systems, generation may take 1-2 minutes.
- **Compatibility**: This project was developed and tested on Windows 10/11. Minor adjustments may be needed for macOS or Linux.
- **Dependencies**: Ensure you have Python 3.8+ and Node.js 16+ installed before running the project.

## Contact Information

For questions or collaboration opportunities:

- **Email**: [EMAIL_ADDRESS]
- **GitHub**: [Your GitHub Profile Link]