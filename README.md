# Player Re-Identification in Football Broadcasts

This project implements real-time object detection and visual re-identification to ensure consistent player tracking across frames — even after occlusions or re-entry into the camera view.

---

## 🎥 Output Videos

- **Detection Output**: [Watch Here](https://drive.google.com/file/d/13kmD6-oK3aXi5eeDLywpmoQw8kwZ852B/view?usp=drive_link) /
   **Detection frames** [ https://drive.google.com/drive/folders/1Xrk7oGRA1XTZMAoiN6NCOWggEV0R3Vi3?usp=sharing ] 
- **Tracking with Re-ID Output**: [Watch Here](https://drive.google.com/file/d/12aCxKEAAmIe_fxovvcP5D956Z371PBvJ/view?usp=drive_link)
  **Tracking with Re-ID Frames**:[  https://drive.google.com/drive/folders/1jTjrXHmQxdmTtUxKKnZSz3SNuFKpilaB?usp=drive_link ]
---

## 📁 Folder Structure

project/
├── assets/
│ ├── 15sec_input_720p.mp4
│ └── best.pt
├── output/
│ ├── detected_frames/
│ ├── tracked_frames/
│ └── tracked_video_reid_final.mp4
├── detect.py
├── track_with_global_reid.py
├── requirements.txt
└── README.md



---

## ⚙️ Setup Instructions

1. **Clone the Repository**  
```bash
git clone https://github.com/Bhavesh9908/Re-Identification.git
cd Re-Identification

2.  Create and Activate a Virtual Environment (Recommended)

python -m venv venv
# Windows
venv\Scripts\activate
# macOS/Linux
source venv/bin/activate

3. Install Dependencies

pip install -r requirements.txt

Alternatively, install manually:
pip install opencv-python torch torchvision numpy pillow scikit-learn ultralytics torchreid

4.  Download YOLOv8 Weights
Place the fine-tuned YOLOv8 best.pt file in the assets/ folder.
(Used for player, referee, goalkeeper, and ball detection)
Download  model: [ https://drive.google.com/file/d/19uuOHJpczzDzAib_pmj6qZ3IFT0Q-RTm/view?usp=sharing ] 

▶️ Running the Code
1. Basic Detection
python detect.py
Output: output/detected_frames/, output/detected_video_custom.mp4

2. Tracking with Global Re-ID
python track_with_global_reid.py
Output: output/tracked_frames/, output/tracked_video_reid_final.mp4

📦 Dependencies
ultralytics>=8.3.152
opencv-python
torch>=1.13
torchvision
numpy
Pillow
scikit-learn
torchreid

📌 Notes
The best.pt file is not included in the repo due to GitHub’s 100MB file limit.

You can download it from this link and place it under assets/.



