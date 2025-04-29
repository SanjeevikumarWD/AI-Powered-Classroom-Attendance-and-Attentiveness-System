# Automated Classroom Attendance and Attentiveness Monitoring System

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-2.0.1-green)](https://flask.palletsprojects.com/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0-orange)](https://www.mysql.com/)

## 📝 Description

This project introduces an innovative solution that streamlines and enhances student attendance tracking and attentiveness monitoring in academic settings. By leveraging advanced facial recognition technology and emotion analysis algorithms, the system provides a seamless, efficient, and accurate method for professors to manage classroom dynamics.


## ✨ Key Features

- **Automated Attendance**: Uses facial recognition to automatically mark attendance
- **Attentiveness Monitoring**: Analyzes student engagement levels during lectures
- **Professor Authentication**: Secure login system for faculty
- **Class Management**: Select subjects and classes for tracking
- **Data Visualization**: Comprehensive reports on attendance and engagement

## 🛠️ Technology Stack

- **Python**: Core programming language
- **Flask**: Web framework for the user interface
- **MySQL**: Database management system
- **YOLO**: Face detection algorithm
- **DeepFace**: Facial recognition and emotion analysis
- **OpenCV**: Computer vision operations

## 🏗️ System Architecture

The system follows a multi-layered architecture:

1. **Face Detection**: Using YOLO to identify faces in classroom images
2. **Face Extraction**: Processing and isolating detected faces
3. **Face Recognition**: Matching faces against a database using Facenet512
4. **Emotion Analysis**: Assessing attentiveness through facial expressions
5. **Data Management**: Storing and retrieving attendance and engagement data

## ⚙️ Implementation Details

- **Data Collection**: Captures and stores student face data with corresponding IDs
- **Face Detection**: Leverages YOLO model for accurate face detection
- **Face Recognition**: Uses DeepFace with Facenet512 for comparing faces against a database
- **Attentiveness Tracking**: Analyzes facial landmarks and emotions to determine engagement levels
- **Attentiveness Calculation**: Computes percentage of attentive students based on emotional states

## 🚀 Installation & Setup

### Prerequisites

- Python 3.8+
- MySQL 8.0+
- Webcam or video input device

### Installation Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/username/classroom-monitoring-system.git
   cd classroom-monitoring-system
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Set up the MySQL database:
   ```bash
   mysql -u root -p < database/schema.sql
   ```

5. Configure the application:
   ```bash
   cp .env.example .env
   # Edit the .env file with your database credentials and other settings
   ```

6. Download the YOLO model:
   ```bash
   python scripts/download_models.py
   ```

7. Run the application:
   ```bash
   python app.py
   ```

## 📊 Usage

### Professor Registration

1. Access the registration page at `/register`
2. Create your account with credentials
3. Log in to access the professor dashboard

### Student Data Collection

1. Navigate to the "Manage Students" section
2. Add new student details (name, ID, class)
3. Capture student face images for the recognition database

### Attendance Tracking

1. Select the subject and class from the dropdown menu
2. Click "Start Attendance" to begin the recognition process
3. The system will automatically detect and mark present students
4. Review and finalize the attendance report

### Attentiveness Monitoring

1. In the dashboard, select "Monitor Attentiveness"
2. Choose the lecture session to monitor
3. The system will analyze student faces for engagement cues
4. View real-time attentiveness percentages and post-session reports

## 📈 Benefits

- **Time-Saving**: Reduces time spent on manual attendance
- **Accuracy**: Minimizes errors in attendance records
- **Insights**: Provides valuable data on student engagement
- **Objective Assessment**: Removes subjectivity in evaluating attentiveness
- **Enhanced Teaching**: Helps instructors identify and address engagement issues

## 🔮 Future Work

- Implementation of more advanced deep learning models for improved recognition
- Individual student attentiveness tracking for personalized interventions
- Multi-language support
- Performance optimization
- Enhanced security measures
- Mobile application development

## 📚 Documentation

For more detailed documentation, please refer to the [Wiki](https://github.com/username/classroom-monitoring-system/wiki) or the `docs/` directory.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 🙏 Acknowledgements

- [OpenCV](https://opencv.org/)
- [DeepFace](https://github.com/serengil/deepface)
- [YOLO](https://github.com/ultralytics/yolov5)
- [Flask](https://flask.palletsprojects.com/)
- [MySQL](https://www.mysql.com/)
