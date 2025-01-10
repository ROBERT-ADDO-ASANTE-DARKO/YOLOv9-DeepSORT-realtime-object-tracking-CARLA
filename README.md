# YOLOv9 and DeepSORT for Real-Time Object Tracking in the CARLA Simulator

## Project Overview

This project integrates the powerful **YOLOv9** object detection algorithm with **DeepSORT** for real-time multi-object tracking within the CARLA Simulator, a leading platform for autonomous vehicle research. The solution is designed to detect and track objects in dynamic environments, enabling advanced perception and trajectory planning.

### Key Features:
- Real-time object detection and tracking using YOLOv9 and DeepSORT.
- Seamless integration with the CARLA Simulator.
- Highly adaptable for autonomous driving research and applications.

### Core Technologies:
- **YOLOv9**: Advanced object detection.
- **DeepSORT**: Robust real-time tracking.
- **CARLA Simulator**: Autonomous driving research simulation.
- **OpenCV**: Image processing.
- **PyTorch**: Deep learning framework.
- **NumPy**: Numerical computations.

https://github.com/user-attachments/assets/9572abdc-eaa7-4baf-94b4-c9dad4d79f10



---

## Installation

### Prerequisites:
- Python **3.7** or higher.
- CARLA Simulator **0.9.11**.

### Installation Steps:

1. **Download and Set Up CARLA Simulator:**
   - Download CARLA 0.9.11 from the [CARLA releases page](https://github.com/carla-simulator/carla/releases).
   - Extract the ZIP file and follow the [CARLA official documentation](https://carla.readthedocs.io/) for installation.
     
   ```bash
   cd CARLA_0.9.11
   ```

2. **Clone This Repository:**
   ```bash
   git clone https://github.com/ROBERT-ADDO-ASANTE-DARKO/YOLOv9-DeepSORT-realtime-object-tracking-CARLA.git
   cd YOLOv9-DeepSORT-realtime-object-tracking-CARLA
   ```

3. **Install Dependencies:**
   Install all required Python libraries:
   ```bash
   pip install -r requirements.txt
   ```

---

## Usage Instructions

### Step 1: Trajectory Planning in CARLA

1. **Copy the trajectory planning script:**
   ```bash
   cp trajectory_planning.py CARLA_0.9.11/PythonAPI/examples/
   ```

2. **Launch the CARLA Simulator:**
   ```bash
   cd CARLA_0.9.11
   ./CarlaUE4.exe
   ./CarlaUE4 -dx11
   ```

3. **Run the trajectory planning script:**
   Open a new terminal, navigate to the CARLA PythonAPI examples directory, and execute the script:
   ```bash
   cd CARLA_0.9.11/PythonAPI/examples
   python trajectory_planning.py
   ```

### Step 2: YOLOv9 and DeepSORT Object Tracking

1. **Clone the YOLOv9 Repository:**
   ```bash
   git clone https://github.com/WongKinYiu/yolov9.git
   cd yolov9
   ```

2. **Prepare the Recorded Video:**
   - Copy the video recorded in CARLA to the YOLOv9 directory.

3. **Add the Tracking Script:**
   - Copy `detect_dual_tracking.py` to the YOLOv9 directory.

4. **Run the Tracking Script:**
   Execute the following command to detect and track objects in the video:
   ```bash
   python detect_dual_tracking.py --weights 'yolov9-c.pt' --source '/yolov9/video.mp4' --device 'cpu'
   ```

---

## Results and Visualizations

This project outputs:
- A video with detected and tracked objects.
- Trajectories and positional data for further analysis.

---

## Contributing

Contributions are welcome! If you'd like to improve this project:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.

---

## License

This project is licensed under the [MIT License](LICENSE).
