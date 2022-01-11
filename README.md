# webcam-object-detection
A repository containing my experiment on implementing Tensorflow 2 Object Detection API on a pre-recorded webcam footage. This notebook was inspired by the original example project at [this link](https://tensorflow-object-detection-api-tutorial.readthedocs.io/en/latest/auto_examples/object_detection_camera.html#sphx-glr-auto-examples-object-detection-camera-py). Instead of using direct webcam access, I tried to use a pre-recorded webcam footage of myself showing several things to the camera.

### Project description
- **TF2 Detection Model Used**: [SSD ResNet V1 FPN 640x640](http://download.tensorflow.org/models/object_detection/tf2/20200711/ssd_resnet101_v1_fpn_640x640_coco17_tpu-8.tar.gz)
- **Input**: Pre-recorded webcam footage (data/videos/webcam.mp4)
- **Process**: 
    - Video was loaded using OpenCV and splitted into frames.
    - Convert each frame into tensor and do prediction.
    - Draw bounding box and labels into the respected frame.
    - Save each processed frame into one folder.
    - Combine all of the frames to create a (result) video with the same FPS as the input video using OpenCV.
    - Save the result video.
- **Output**: The same webcam footage with boxes and label prediction (data/videos/result_webcam.avi)

