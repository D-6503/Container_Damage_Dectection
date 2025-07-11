# Damage Detection with YOLOv8

A Streamlit web application for detecting damage in images using a pre-trained YOLOv8 model. Users can upload an image, view the detected damage with labeled bounding boxes (showing only damage types), and see detailed detection data in a table.

## Features
- Upload images (JPG, JPEG, PNG) for damage detection.
- Display annotated images with bounding boxes labeled by damaged.
- Show a table with detection details: Detection #, Damaged, Confidence, and Bounding Box coordinates.
- Built with Streamlit for an interactive web interface.
- Uses a custom YOLOv8 model (`best.pt`) for damage detection.

## Sample Outputs
![image](https://github.com/user-attachments/assets/eea5fe3d-18d1-408f-8d8f-ff91e7c9b81f)
![image](https://github.com/user-attachments/assets/464e0abd-f439-4b72-9854-77893b57cb96)

## Prerequisites
- Python 3.8 or higher
- A trained YOLOv8 model file (`best.pt`) in the project directory
- Git (for cloning the repository)

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/iamsonuram/Container__Damage_Detection.git
   cd Container_Damage_Detection
   ```

2. **Create a virtual environment** *(optional but recommended)*:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Ensure the YOLOv8 model**:
   - Place your `best.pt` file in the project root or update the path in `app.py` if stored elsewhere.

## Usage

Run the Streamlit app:
```bash
streamlit run app.py
```

Access the app:
- Open your browser and go to `http://localhost:8501`
- Upload an image to detect damage
- View the annotated image with damage labels and a table of detection details below

## Project Structure
```
your-repo-name/
│
├── home.py              # Main Streamlit application
├── pages
    ├── result.py
├── best.pt              # YOLOv8 model file (not tracked in Git)
├── requirements.txt     # Python dependencies
├── README.md            # Project documentation
```

## Notes
- The app assumes `best.pt` outputs bounding boxes with class labels. Adjust `app.py` if your model has a different format.
- For large images, consider adding resizing logic in `app.py` to improve performance.
- To customize the UI (e.g., bounding box colors, table format), modify `app.py`.

## Acknowledgments
- Built with Streamlit and Ultralytics YOLOv8.
- Thanks to the open-source community for robust tools!
