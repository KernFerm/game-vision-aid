# 🎮 GameVisionAid

**GameVisionAid** is an accessibility tool designed to assist visually impaired gamers by enhancing visual cues in video games. It uses real-time object detection to create customizable overlays around enemy players, making it easier to identify and engage with them during gameplay.

## 🚀 Features

- 🖥️ **Real-Time Screen Capture**: Captures your screen in real-time using `mss` for fast and efficient screen capturing.
- 🎯 **Object Detection**: Utilizes YOLOv5 for detecting enemies in video games.
- 🟩 **Customizable Overlays**: Allows users to choose the color of the overlay boxes around detected enemies.
- 🛠️ **GPU Acceleration**: Supports GPU acceleration for faster processing with CUDA-enabled GPUs.

## 🖥️ System Requirements

- **Operating System**: Windows, Linux, or macOS
- **Python Version**: Python 3.7 or higher
- **Hardware**:
  - **CPU**: Multi-core processor (Intel i5 or equivalent)
  - **GPU** (Optional, but recommended for better performance): NVIDIA GPU with CUDA support
  - **RAM**: 8 GB or more

## 📦 Installation

Follow these steps to set up and run **GameVisionAid**:

1. **Clone the repository**:
    ```
    git clone https://github.com/kernferm/game-vision-aid.git
    cd game-vision-aid
    ```

2. **Set up a virtual environment (optional but recommended)**:
    ```
    python -m venv gamevisionaid_env
    source gamevisionaid_env/bin/activate  # On Windows use: gamevisionaid_env\Scripts\activate
    ```

3. **Install dependencies**:
    ```
    pip install -r requirements.txt
    ```

   If you don't have a `requirements.txt` file, you can install dependencies manually:
    ```
    pip install opencv-python torch torchvision onnxruntime numpy pandas gitpython tk mss
    ```

4. **For GPU Support (Optional)**:
   - If you have a CUDA-enabled GPU, install the version of PyTorch that supports your CUDA version:
     ```
     pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
     ```
     Replace `cu118` with your CUDA version. 
     - Use the `install_pytorch.bat` is tied to `cu118`.

## 📝 Usage

1. **Run the GameVisionAid script**:
    ```
    python main.py
    ```

2. **Select the overlay color**:
   - A prompt will appear. Enter the color name you want for the overlay boxes around detected enemies. You can type "exit" or "q" to quit the program.

3. **Start your game**:
   - The overlay will run in parallel with your game, highlighting detected enemies with the chosen color.

4. **Exit the overlay**:
   - Press `q` at any time to close the overlay and exit the program.

## 📂 Project Structure

```
game-vision-aid/ 
│ 
├── README.md                # Project documentation 
├── game_overlay.py          # Main script file 
├── requirements.txt         # List of required Python packages 
└── model/                   # Directory to store custom YOLOv5 models (if any) 
    └── best.pt              # Custom YOLOv5 model (if available)
```


## 🤖 Custom YOLOv5 Model (Optional)

If you have a custom-trained YOLOv5 model specifically for your game:

1. Place your `.pt` or `.onnx` file in the `model/` directory.
2. Update the `main.py` script to load your custom model:
    ```
    model_path = 'model/best.pt'  # or 'model/best.onnx'
    ```

## ❗ Known Issues
- **Performance on CPU:** The overlay may run slower on systems without a GPU. Using a CUDA-enabled GPU is recommended for real-time performance.
- **Compatibility:** This tool is intended for games that allow screen capturing and do not violate any terms of service.

## 🛠️ Contributing

- Contributions are welcome! Feel free to submit a pull request or open an issue to discuss improvements, bugs, or new features.

## 📜 License

This project is proprietary and all rights are reserved by the author. Unauthorized copying, distribution, or modification of this project is strictly prohibited. Unless You have written permission from the Developer or the FNBUBBLES420 ORG.  

## 📧 Contact

- [Bubbles The Dev](kernferm@gmail.com)
- [Main Office](mainoffice@fnbubbles420.org)
## 🙏 Acknowledgements

Thanks to the developers of:
- [YOLOv5](https://github.com/ultralytics/yolov5)
- [mss](https://github.com/BoboTiG/python-mss)

-----

# 👨‍💻 Developed by [Bubbles The Dev](https://github.com/kernferm) - Making gaming more accessible for everyone!

-----

## ⚠️ Disclaimer

**GameVisionAid** is designed to assist visually impaired or color-blind gamers by enhancing visual cues in video games. It uses real-time object detection to create customizable overlays around enemy players, making it easier to identify and engage with them during gameplay.

This tool runs in parallel with any game and does not modify the game files or violate any terms of service. It captures the screen and provides an overlay to help users better perceive in-game elements. The developer is not responsible for any misuse of this tool.