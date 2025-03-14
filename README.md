# smartTraffix 🚦  
 AI-Powered Traffic Monitoring and Violation Detection System  

 📌 Overview  
smartTraffix is an AI-driven Automatic Traffic Monitoring System that integrates multiple computer vision-based traffic management features. It can detect violations, recognize vehicle license plates, count vehicles, and generate insightful heatmaps for traffic analysis.  

 🚀 Features  
 🔍 Detection Capabilities:  
✅ Helmet Detection – Identifies riders without helmets.  
✅ Triple Riding Detection – Detects more than two passengers on a two-wheeler.  
✅ Accident Detection – Automatically flags accidents on the road.  
✅ Overspeeding Detection – Monitors vehicle speed violations.  
✅ Heatmap Visualization – Generates traffic heatmaps from video data.  
✅ Emergency Vehicle Detection – Detects ambulances and other priority vehicles.  
✅ Crosswalk Detection – Ensures pedestrian safety by monitoring crosswalk usage.  

 🛠 Live Traffic Monitoring:  
✅ Automatic Number Plate Recognition (ANPR) – Extracts vehicle registration details.  
✅ Automatic Traffic Counting & Classification (ATCC) – Counts vehicles and classifies them into categories (cars, buses, bikes, etc.).  

 📂 Project Structure  

smartTraffix/
│── app.py                      # Flask backend for API requests  
│── requirements.txt             # Dependencies for the project  
│── uploads/                     # Directory to store uploaded videos  
│── Helmet_Detector.py           # Helmet detection script  
│── TripleRiding.py              # Triple riding detection script  
│── Accident_Detector.py         # Accident detection script  
│── Overspeeding.py              # Speed monitoring script  
│── Heatmap_Visualizer.py        # Traffic heatmap generator  
│── Emergency_Vehicle_Detector.py# Emergency vehicle detection  
│── Crosswalk.py                 # Crosswalk monitoring  
│── ANPR.py                      # Automatic Number Plate Recognition  
│── ATCC.py                      # Automatic Traffic Counting and Classification  
│── README.md                    # Project documentation  


 ⚙️ Installation & Setup  
 1️⃣ Clone the Repository  

git clone https://github.com/YOUR_USERNAME/smartTraffix.git
cd smartTraffix


 2️⃣ Install Dependencies  
Ensure you have Python 3.9+ installed. Then, install the required libraries:  

pip install -r requirements.txt


 3️⃣ Run the Flask Backend  

python app.py

The backend will start on http://0.0.0.0:5000/.

 🎯 API Usage  
 1️⃣ Check Server Status  

GET http://localhost:5000/

Response:  
json
{"message": "Flask backend is running!"}


 2️⃣ Process a Video (ANPR/ATCC)  

POST http://localhost:5000/process

Form Data:  
- process: "ANPR" or "ATCC"  
- videos: Upload video file(s)  

 3️⃣ Process a Feature Detection Video  

POST http://localhost:5000/process

Form Data:  
- feature: One of the detection features (e.g., "Helmet Detection")  
- video: Upload a single video  
 

 📜 License  
This project is licensed under the MIT License.  

