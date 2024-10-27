# Football Analysis System Using YOLO, Optical Flow, and Perspective Transformation

## 1. Introduction
**Objective:** Create a system that detects and tracks players, referees, and footballs on the field, assigns players to teams based on t-shirt color, and calculates each player’s speed and distance covered.

**Technologies:** Machine Learning, Computer Vision, Deep Learning, YOLO, Optical Flow, Perspective Transformation.

## 2. Components of the System

<details>
<summary>⚙️ YOLO Object Detection</summary>

- Using YOLO (You Only Look Once) to detect objects like players, referees, and footballs in video frames.
- **Steps:**
    - Use pre-trained YOLOv8 for initial detection.
    - Train a custom YOLO model to improve accuracy for your specific dataset.
</details>

<details>
<summary>📍 Trackers</summary>

- Track detected objects across multiple video frames to ensure continuity in tracking each player, referee, and football.
</details>

## 3. Player Team Assignment Using T-shirt Color

<details>
<summary>🎨 KMeans for Pixel Segmentation</summary>

- Cluster pixels to segment player t-shirts from the background.
- Assign each player to a team based on t-shirt color.
</details>

## 4. Camera Movement and Player Tracking

<details>
<summary>🎥 Optical Flow</summary>

- Measure the camera's movement between frames.
- Helps in differentiating camera motion from player motion.
</details>

## 5. Depth and Distance Calculation

<details>
<summary>📏 Perspective Transformation</summary>

- Convert 2D pixel data into 3D space to measure actual distances (in meters) on the field.
- Accurately represent depth in video frames using OpenCV’s `cv2.perspectiveTransform`.
</details>

## 6. Player Speed and Distance Measurement

<details>
<summary>🚀 Speed Calculation</summary>

- Measure player movement across frames and calculate speed in meters per second.
- **Formula:** `Speed = Distance / Time` (based on perspective-transformed measurements).
</details>

<details>
<summary>📍 Distance Covered</summary>

- Calculate the total distance each player covers during the game using tracked positions over time.
</details>

## 7. System Workflow

<details>
<summary>📈 Workflow Overview</summary>

1. **Input**: Video footage of a football match.
2. **Object Detection**: YOLO detects players, referees, and the football.
3. **Tracking**: Track each object across frames.
4. **Team Assignment**: Use KMeans to segment players by t-shirt color.
5. **Camera Adjustment**: Apply optical flow to adjust for camera movements.
6. **Distance & Speed Calculation**: Use perspective transformation and tracking to measure player movements.
</details>

## 8. Challenges & Solutions

<details>
<summary>🛠️ Common Challenges</summary>

- **Occlusion Handling**: Manage situations when players overlap in video frames.
- **Lighting Variations**: Adapt to different lighting conditions affecting object detection and t-shirt color segmentation.
</details>

## 9. Conclusion
A comprehensive system that combines various techniques to solve real-world football analysis problems. Enhances game analysis by tracking player movements, detecting teams, and measuring performance metrics like speed and distance.

---

Feel free to explore each component and follow the steps to gain insights into the functionalities and challenges of this football analysis system.
