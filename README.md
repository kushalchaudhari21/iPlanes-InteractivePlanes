## Description
This is a code written in Python that can turn any surface in the world into an interactive interface.

The use case for this project is the classic projected screens on a wall using a projector. The code converts the traditional non-interactive projectors into an interactive interface for the the end user. It helps us to be more involved with content projected on screen and connect with audience better by eliminating the interactions with laptops. We accomplish this by using simple image processing/computer vision algorithms, thereby, eliminating the need for any additional hardware sensors. Therefore the cost of the system is equivalent to cost of a small push button switch and an LED(<1$) compared to 1000-3000$ for interactive whiteboards.

![Output](https://github.com/kushalchaudhari21/iPlanes-InteractivePlanes/blob/master/data/result.png)

The **video** on the working of this system can be found [here](https://www.linkedin.com/feed/update/activity:6468389723479080960/).

Hardware dependencies :

- Webcam (internal laptop webcam or usb webcam).
- LED pen with a push-button switch.

Software Dependencies:
- Python.
- pyautogui.
- pynput.
- OpenCV.

## Sample Invocation

**1.** Install the dependencies (Ubuntu or MacOS is preffered)

```bash
  sudo apt-get install python-dev python-pip python-wheel
  pip install numpy
  pip install pyautogui
  sudo -H python -m pip install --upgrade pip setuptools wheel 
  sudo -H pip install xlib
  sudo -H pip install xlib>=0.17
  sudo -H pip install pynput
  pip install opencv-contrib-python
```
You can also follow through different OpenCV installation tutorials on [pyimagesearch](https://www.pyimagesearch.com) to get OpenCV on your system.

**2.** In the terminal, in the project directory input the following to execute the script
```console
python source.py
```
## Usage

**1.** System Arrangement -

Keep the camera faced to the projected surface and keep it fixed. 

![SystemInterface](https://github.com/kushalchaudhari21/iPlanes-InteractivePlanes/blob/master/data/system_arrangement.png)

**2.** Run the code as per sample invocation. Then select the four points in image that pops up in the following order to define the region of interest : top-left, top-right, bottom-left, bottom-right.

**3.** Once you select the four points the image disappears and the interface is active. Sample usage:

Clicking -

![Clicking](https://github.com/kushalchaudhari21/iPlanes-InteractivePlanes/blob/master/data/1.gif)

Opening files applications and folders -

![Clicking2](https://github.com/kushalchaudhari21/iPlanes-InteractivePlanes/blob/master/data/2.gif)

Drawing or Writing -

![WriteDraw](https://github.com/kushalchaudhari21/iPlanes-InteractivePlanes/blob/master/data/3.gif)

## Important Insights

* Order in which points are selected can be changed using different value of pointIndex.
* The basic LED schematic is as follows:

![Pen](https://github.com/kushalchaudhari21/iPlanes-InteractivePlanes/blob/master/data/pen_schematic.png)

* Scope of future development lies in using deeplearning algorithms to come up with a complete touchscreen interface. Thereby, eliminating the need for the LED pen. Also the perspective transform can be automatic after certain refresh rates which will provide consistency even if the webcam is disturbed slightly. 
* You can also refer to the [Report](https://github.com/kushalchaudhari21/iPlanes-InteractivePlanes/blob/master/ProjectReport.pdf) for additional information.
