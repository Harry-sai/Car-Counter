# Project1-Car: Vehicle Counting with YOLOv8 + SORT

This project detects and tracks road vehicles (`car`, `bus`, `truck`, `motorbike`) from a video and counts them when they cross a defined line.

It also saves the processed output video with overlays and count.

## Features

- YOLOv8 object detection using `ultralytics`
- Multi-object tracking with `SORT`
- Line-crossing based vehicle counting
- Live display window
- Saved output video (`.mp4`)

## Project Files

- `car_counter.py`: main script
- `sort.py`: SORT tracker implementation
- `mask.png`: region-of-interest mask
- `graphics.png`: UI overlay graphics
- `video/cars.mp4`: input video (local)
- `output_car_counter.mp4`: generated output video

## Requirements

Install dependencies from:

```bash
pip install -r requirements.txt
```

Main packages used:

- `ultralytics`
- `opencv-python`
- `cvzone`
- `torch`, `torchvision`
- `numpy`
- `filterpy`, `lap`, `scikit-image`

## How to Run

Run from repository root (`Object_detection`):

```bash
python Project1-Car/car_counter.py
```

Press `q` to stop the app.

## Input and Output Paths (Current Script)

- Input video: `Video/cars.mp4`
- Model weights: `model/yolov8l.pt`
- Output video: `output_car_counter.mp4`


## Notes

- The script is currently written for Windows-style paths.
- On Linux/macOS, path case matters (`Video` vs `video`), so update paths if needed.
- If CUDA is available, inference runs on GPU automatically; otherwise CPU is used.
