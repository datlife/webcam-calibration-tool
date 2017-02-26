# Webcam Calibration Tool
=========================
**Status** : BUILDING

One of the steps before using the camera as "eyes" for your robot is to calibrated it. The reason is due to distortions of the camera. One solution is to calibrate your webcam.

This tool is an easy-to-use that return two things: the camera_matrix and distortion_coefficients matrix. (Why? Take a look [here](http://docs.opencv.org/2.4/doc/tutorials/calib3d/camera_calibration/camera_calibration.html?)  ).

![alt-tex](https://github.com/dat-ai/webcam-calibration-tool/raw/master/docs/result.JPG)
### How To Use (Current updating)
--------------
1. Compile the C++ file into executable file.
2. Run command
```shell
calibrate path_to_images num_chess_rows num_chess_cols
```
3. The program will save an XML file in the same directory `calibration_matrix.xml`.
4. That's it. Now you just need use these matrices in `cv::undistort()` function to get calibrated image.

