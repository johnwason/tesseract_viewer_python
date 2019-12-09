# tesseract_viewer_python

`tesseract_viewer_python` is a proof of concept viewer for the [ROS Industrial Tesseract planning environment](https://github.com/ros-industrial-consortium/tesseract) [Python wrappers](https://github.com/johnwason/tesseract_python) using the [Babylon.js](https://github.com/BabylonJS) WebGL game engine. This viewer works by starting a small web server on a local port (default TCP port 8000), and serving the necessary files to display the geometry and the currently active trajectory. A modern web browser can then be used for display. The browser will poll once a second to see if the trajectory or geometry have changed. The trajectory will automatically update. A change in the scene geometry will cause a reload.

This project is a simple *proof of concept* and has a very limited feature set.

## Example

Examples can be found in the `examples` directory. To run the `abb_irb2400_viewer.py` example in a ROS environment, run:

    source ~/catkin_ws/devel_isolated/tesseract_python/setup.bash
    export TESSERACT_SUPPORT_DIR=~/catkin_ws/devel_isolated/tesseract_support/share/tesseract_support
    export PYTHONPATH=$PYTHONPATH:.
    python examples/python examples/abb_irb2400_viewer.py

Now point a web browser to `http://localhost:8000`

## Oculus Quest

Thanks to the WebVR/WebXR support in Babylon.js, the viewer can be used with VR headsets including Oculus Quest. Using the [Firefox Reality](https://www.oculus.com/experiences/quest/2180252408763702/?locale=en_US) browser on the Oculus Quest, navigate to the viewer address. An example address would be `http://192.168.1.22:8000`. Substite 192.168.1.22 for your computer's IP address. Once on the viewer page, a goggles symbol should be visible on the lower right of the page. Clock the goggle symbol to enter VR.

## License

Apache 2.0

`tesseract_viewer_python` is developed by Wason Technology, LLC
