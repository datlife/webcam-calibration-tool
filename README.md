# Webcam Calibration Tool
=========================
**Status** : BUILDING

One of the steps before using the camera as "eyes" for your robot is to calibrate it. The reason is camera has distortions. These distortions would not let your robot see the real picture of surroundings.

This tool is an easy-to-use that return two things: the camera_matrix and distortion_coefficients matrix. (Why? Take a look [here](http://docs.opencv.org/2.4/doc/tutorials/calib3d/camera_calibration/camera_calibration.html?)  ).

![alt-tex](https://github.com/dat-ai/webcam-calibration-tool/raw/master/docs/result.JPG)
### How To Use (Current updating)
--------------
  * Compile the C++ file into executable file.
  * Run command
```shell
calibrate path_to_images num_chess_rows num_chess_cols
```
  * The program will save an XML file in the same directory `calibration_matrix.xml`.
  * That's it. Now you just need use these matrices in `cv::undistort()` function to get a calibrated image.

