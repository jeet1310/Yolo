# Object Detection and Identification using YOLO in MATLAB

## Overview
This project utilizes the YOLO (You Only Look Once) object detection model in MATLAB to detect and identify objects in both images and videos. The project leverages the pre-trained Tiny-YOLOv3 model from the COCO dataset for efficient and accurate object detection.

## Features
- Object detection on static images
- Object detection on video streams
- Counting the number of detected objects
- Filtering weak detections based on confidence threshold
- Displaying bounding boxes and confidence scores on detected objects
- Saving the processed video with annotations

## Requirements
To run this project, ensure that you have:
- MATLAB with Deep Learning Toolbox
- Computer Vision Toolbox
- Image Processing Toolbox
- A pre-trained YOLO model (`tiny-yolov3-coco`)
- Input image (`dp.jpeg`) and video file (`cars.mp4`)

## Installation
1. Clone this repository:
   ```sh
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```
2. Open MATLAB and navigate to the project folder.
3. Ensure that the required toolboxes are installed.

## Usage
### Running Object Detection on an Image
1. Place your input image (`dp.jpeg`) in the project folder.
2. Run the MATLAB script to process the image:
   ```matlab
   model = 'tiny-yolov3-coco';
   detector = yolov3ObjectDetector(model);
   inputImage = imread('dp.jpeg');
   [bboxes_img, scores_img, labels_img] = detect(detector, inputImage);
   ```
3. The detected objects and total count will be displayed.

### Running Object Detection on a Video
1. Place your input video file (`cars.mp4`) in the project folder.
2. Run the script to process the video:
   ```matlab
   videoSource = vision.VideoFileReader('cars.mp4');
   videoPlayer = vision.VideoPlayer('Position', [100, 100, 680, 480]);
   ```
3. The processed video with object annotations will be saved as `output_video.avi`.

## Output
- **Image Processing Output:** The script will display the image with detected objects and their labels.
- **Video Processing Output:** The script will process the video frame-by-frame, detect objects, annotate frames, and save the output video.

## Customization
- To use a different image, replace `dp.jpeg` with your image file.
- To use a different video, replace `cars.mp4` with your video file.
- Modify the confidence threshold in the script:
  ```matlab
  confidenceThreshold = 0.5; % Adjust as needed
  ```

## Future Enhancements
- Implement real-time object detection using a webcam.
- Improve accuracy with a larger YOLO model (e.g., YOLOv4 or YOLOv5).
- Integrate tracking algorithms for object movement analysis.

## License
This project is open-source and available under the MIT License.

## Author
Jeet Jain


