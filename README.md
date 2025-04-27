# S4 Slicer
A generic non-planar slicer, that can print almost any part without support.

Please use the [dicussions tab](https://github.com/jyjblrd/S4_Slicer/discussions) to ask questions and help others.

[Try it now](https://colab.research.google.com/github/jyjblrd/S4_Slicer) on Google Colab! (note: colab free tier is only powerful enough to slice very simple models)

[![Watch the video](https://github.com/jyjblrd/S4_Slicer/blob/main/thumnail.jpeg?raw=true)](https://www.youtube.com/watch?v=M51bMMVWbC8)

Check out my [YouTube video](https://youtu.be/M51bMMVWbC8?si=pfud7bHgjYDnO2_z) for more details!

Thank you to JLCCNC for helping create the extruder mount and build plate for my [4 Axis Core R-Theta Printer](https://github.com/jyjblrd/Core-R-Theta-4-Axis-Printer).

## Local Usage (on your own PC)
Install and configure Python 3 and Jupyter Notebook ([see guide](https://gist.github.com/PixlRainbow/c9a75f4ccbea98c357db9e4d61c11cf8)), then open the `main.ipynb` file.  
Do not run the cell that contains `!apt-get install -qq xvfb libgl1-mesa-glx`; assuming you are using Linux, instead install `xvfb` and `libgl1-mesa-glx` from a separate terminal window, with administrative permissions as required. If you are using a Linux distribution with a graphical interface, or if you are using Windows, installation of these two libraries may not be needed at all.



Bibtex Citation:
```
@software{Bird_S4_Slicer,
author = {Bird, Joshua},
license = {GPL-3.0},
title = {{S4 Slicer}},
url = {https://github.com/jyjblrd/S4_Slicer}
}
```
