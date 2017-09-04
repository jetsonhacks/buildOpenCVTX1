License: MIT. See license file in root directory
Copyright(c) JetsonHacks (2017)
Copyright(c) Peter Moran (2017)

There are two example programs here. Both programs require OpenCV to be installed with GStreamer support enabled.
Both of these examples were last tested with L4T 28.1, OpenCV 3.3

The first is a simple C++ program to view the onboard camera feed from the Jetson Dev Kit.

To compile gstreamer_view.cpp:

$ gcc -std=c++11 gstreamer_view.cpp -o gstreamer_view -L/usr/lib -lstdc++ -lopencv_core -lopencv_highgui -lopencv_videoio

to run the program:

$ ./gstreamer_view

The second is a Python program that reads the onboard camera feed from the Jetson Dev Kit and does Canny Edge Detection.

To run the Canny detection demo:

$ python cannyDetection.py

Notes:
1. OpenCV4Tegra does not have GStreamer support enabled, and therefore will not run these demos
2. The gstreamer_view example is from Peter Moran:
   https://gist.github.com/peter-moran/742998d893cd013edf6d0c86cc86ff7f
   Note that the nvvidconv flip-method was changed to 0. Earlier versions of L4T used a flip method of 2. 



