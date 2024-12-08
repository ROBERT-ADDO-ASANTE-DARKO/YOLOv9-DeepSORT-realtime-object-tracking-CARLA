#   YOLOv9 and DeepSORT for Real-Time Object Tracking in the CARLA Simulator

## Project Overview

This project leverages the cutting-edge YOLOv9 object detection algorithm combined with DeepSORT for real-time multi-object tracking in CARLA Simulator footage.

### Key Technologies:
- YOLOv9 (You Only Look Once, version 9)
- DeepSORT (Deep Simple Online and Realtime Tracking)
- CARLA Simulator
- OpenCV
- PyTorch
- NumPy
  
## Installation

### Prerequisites:
- Python 3.7 or higher
- CARLA Simulator 0.9.11

### Steps:

1. Download the required version of the CARLA Simulator ZIP file for Windows:
   https://github.com/carla-simulator/carla/releases
   ```
   cd CARLA_0.9.11
   ```

3. Install CARLA_0.9.11 following the official documentation.

4. Clone this project repository:
   ```
   https://github.com/ROBERT-ADDO-ASANTE-DARKO/Autonomous-Vehicle-Object-Detection-and-Trajectory-Planning-using-YOLOv3-and-CARLA-Simulator.git
   cd Autonomous-Vehicle-Object-Detection-and-Trajectory-Planning-using-YOLOv3-and-CARLA-Simulator
   ```

5. Install the required Python libraries:
   ```
   pip install -r requirements.txt
   ```

## Usage

1. Copy the `object_detection.py` file to the CARLA PythonAPI examples directory:
   ```
   cp object_detection.py CARLA_0.9.11/PythonAPI/examples/
   ```

2. Download the yolov3.weights and yolo3.cfg files
   https://huggingface.co/spaces/Epitech/Scarecrow/resolve/main/yolov3.weights
   https://www.kaggle.com/datasets/ravi02516/trained-weights-and-cfg?select=yolov3.cfg

4. Run the CARLA Simulator:
   ```
   cd CARLA_0.9.11
   ./CarlaUE4.exe
   ./CarlaUE4 -dx11
   ```

5. In a new terminal, navigate to the PythonAPI examples directory and run the script:
   ```
   cd CARLA_0.9.11/PythonAPI/examples
   python object_detection.py
   ```

## Monitoring Model Performance

To monitor and track the YOLOv3 model performance using TensorBoard:

1. Start TensorBoard:
   ```
   tensorboard --logdir=path/to/logs
   ```

2. Open a web browser and go to `http://localhost:6006` to view the TensorBoard dashboard.

## Project Structure

- `object_detection.py`: Main Python script for object detection and trajectory planning
- `requirements.txt`: List of required Python libraries
- `models/`: Directory containing trained YOLOv3 model weights
- `config/`: Directory containing trained YOLOv3 model configurations
- `logs/`: TensorBoard log files for performance monitoring

## Contributing

Contributions to improve the project are welcome. Please feel free to fork the repository, make changes, and submit a pull request.

## License
