# License Plate Recognition using YOLO and OCR

## Project Overview
This project implements a robust **License Plate Recognition** (LPR) system using the **YOLOv8** deep learning model for license plate detection and **Tesseract OCR** for text extraction. The project is designed to analyze video feeds, detect license plates in real-time, and extract readable text from the plates. It also maps the extracted license plate text to corresponding states in India and logs this data for future use.

### Key Features
- **High-Precision License Plate Detection**: Utilizes the YOLOv8 model to accurately detect license plates in various scenarios.
- **Optical Character Recognition (OCR)**: Leverages Tesseract OCR to extract text from detected license plates.
- **State Identification**: Maps detected license plate numbers to Indian states.
- **Real-Time Processing**: Handles video streams frame-by-frame for live recognition.
- **Data Export**: Saves detected license plate numbers along with the timestamp and state information to an Excel file.

## Project Structure
The project structure is organized as follows:

```
├── License_Plate_Recognition
│   ├── car_plate_recognition.py       # Main script file for the LPR system
│   ├── README.md                      # Documentation file
│   ├── requirements.txt               # Required dependencies
│   ├── coco.txt                       # COCO class list for YOLO model
│   ├── best.pt                        # Pretrained YOLOv8 model file
│   ├── carsfinals.xlsx                # Output Excel file for license plate data
│   └── mycarplate.mp4                 # Sample video file for testing
```

## Installation
Follow these steps to set up the project locally:

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/LicensePlate-Recognition.git
   cd LicensePlate-Recognition
   ```

2. **Create and activate a virtual environment (optional but recommended):**

   ```bash
   python -m venv venv
   source venv/bin/activate  # For Linux/Mac
   venv\Scripts\activate     # For Windows
   ```

3. **Install the dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Download Tesseract:**
   Install Tesseract OCR on your machine. For Linux, use:

   ```bash
   sudo apt install tesseract-ocr
   ```

   For Mac, use:

   ```bash
   brew install tesseract
   ```

   Make sure to set the correct path for `tesseract_cmd` in the code.

5. **Download the YOLO Model:**
   - Ensure `best.pt` is placed in the correct directory (`/path/to/best.pt`).
   - You can modify the path in the code to point to your YOLO model file.

6. **Run the project:**

   ```bash
   python car_plate_recognition.py
   ```

## Dependencies
- `opencv-python`
- `pandas`
- `ultralytics`
- `numpy`
- `pytesseract`
- `datetime`

To install the above dependencies, use:

```bash
pip install opencv-python pandas ultralytics numpy pytesseract
```

## Usage
- The script processes video frames to detect license plates.
- Detected plates are logged in an Excel file named `carsfinals.xlsx` with the following columns:
  - `NumberPlate`
  - `Date`
  - `Time`
  - `State`

### How to Modify
- Replace the path of `mycarplate.mp4` in the script with your own video file path.
- Adjust the ROI (region of interest) to detect plates in a specific area of the frame.

## Example Output
The detected license plates, along with their timestamps and states, will be saved in the Excel file `carsfinals.xlsx`.

## Project Improvements
Potential improvements for this project include:
- **Implementing multiple language OCR** to handle plates from various regions.
- **Improving detection accuracy** using a larger and more diverse dataset.
- **Adding a GUI** for easier visualization and analysis.

## Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact
For any questions or feedback, reach out at `your.email@example.com`.

---

Feel free to modify the content as per your project requirements and structure.
