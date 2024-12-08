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

2. Install CARLA_0.9.11 following the official documentation.

3. Clone this project repository:
   ```
   https://github.com/ROBERT-ADDO-ASANTE-DARKO/Autonomous-Vehicle-Object-Detection-and-Trajectory-Planning-using-YOLOv3-and-CARLA-Simulator.git
   cd Autonomous-Vehicle-Object-Detection-and-Trajectory-Planning-using-YOLOv3-and-CARLA-Simulator
   ```

4. Install the required Python libraries:
   ```
   pip install -r requirements.txt
   ```

## Usage

1. Copy the `trajectory_planning.py` file to the CARLA PythonAPI examples directory:
   ```
   cp trajectory_planning.py CARLA_0.9.11/PythonAPI/examples/
   ```

2. Run the CARLA Simulator:
   ```
   cd CARLA_0.9.11
   ./CarlaUE4.exe
   ./CarlaUE4 -dx11
   ```

3. In a new terminal, navigate to the PythonAPI examples directory and run the script:
   ```
   cd CARLA_0.9.11/PythonAPI/examples
   python trajectory_planning.py
   ```

## YOLOv9 and DeepSORT object tracking

1. Clone the YOLOv9 GitHub repository:
   ```
   https://github.com/WongKinYiu/yolov9
   cd yolov9
   ```

2. Copy the recorded video in CARLA and paste it in the yolov9 directory.
   
3. Copy the `detect_dual_tracking.py` file to the yolov9 directory.

4. In a new terminal, navigate to the yolov9 directory and run the script:
   ```
    python detect_dual_tracking.py --weights 'yolov9-c.pt' --source '/yolov9/video.mp4' --device 'cpu'
   ```

## Contributing

Contributions to improve the project are welcome. Please feel free to fork the repository, make changes, and submit a pull request.

## License
