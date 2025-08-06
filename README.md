# License-Plate-Reader-In-Video-Using-YOLOv8

In this repository is implemmented the license plate  reading project by [Computer Vision Engineer](https://youtu.be/fyJB1t0o0ms?si=wuu3bamSpUVoOi60) in a Jupyter notebook. 

<img src="im/cars.jpg" alt="CARS" width="500" />

The project uses the following components:
- YOLOv8 nano to detect cars
- A custom license plate detector (based on YOLOv8) implemented in a previous [repository](https://github.com/GerardoRodriguezB/License-Plate-Detector-Using-YOLOv8)
- [EasyOCR](https://github.com/JaidedAI/EasyOCR) to read the license plates
- [SORT](https://github.com/abewley/sort) for tracking cars accross frames.

## Environment Setup

You can reuse the same Anaconda environment created for the license plate detector in the previous [repository](https://github.com/GerardoRodriguezB/License-Plate-Detector-Using-YOLOv8). Then, install the required packages by running:

```bash
pip install -r requirements.txt
```

Clone the SORT repository into the root of this project. 

```bash
git clone https://github.com/abewley/sort.git
```

Place your trained license plate detection model in a folder called `model`, and name the file `plate_detector.pt`.



## Install PyTORCH

If your machine has a CUDA compatible GPU, install:

```bash
pip install torch==2.5.1 torchvision==0.20.1 torchaudio==2.5.1 --index-url https://download.pytorch.org/whl/cu118
```

Otherwise, install the CPU versions:

```bash
pip install torch==2.5.1 torchvision==0.20.1 torchaudio==2.5.1
```

## Video Setup

Download the video used in this project from this [link](https://www.pexels.com/video/traffic-flow-in-the-highway-2103099/). Rename the file to cars.mp4 and place it in a folder named video.

## Output

After running the notebook, a processed video named `cars_processed.mp4` will be saved in the `video` folder.
A short fragment of the output video is included in this repository as an example.






