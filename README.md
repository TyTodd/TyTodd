👋 Hi, I’m @TyTodd welcome to my github. Some of my favorite projects on here:
## [modaic](https://github.com/modaic-ai/modaic)
A python SDK for agent orchestration, context engineering, version control and optimization.
## [datasets #7616](https://github.com/huggingface/datasets/pull/7616) 
A PR I made to the datasets library to make it easier to work with multi-modal video and audio datasets. By adding audio and video decoding using torchcodec supporting decoding audio tensors directly from video as well as CUDA accelerated video decoding. Released in datasets 4.0.0

## [py5-layout](https://github.com/TyTodd/py5-layout)
React Native's yoga layout manager for py5 turns this
You can also embed custom animations and renderings into the layout. See the [custom sketch example](./examples/custom_sketch.py)

```python
import py5
from py5_layout import Py5Layout, Div, Style, Text, Element
from math import sin, cos
from time import time
width_ = 500
height_ = 500
layout = None
last_print_time = 0

class CustomSketch(Element):
    def __init__(self, circle_radius: int, circle_color: tuple, **kwargs):
        super().__init__(**kwargs)
        self.circle_radius = circle_radius
        self.circle_color = circle_color

    def draw(self):
        with self.canvas(set_origin=False, clip=True):
            py5.fill(*self.circle_color)
            py5.circle(py5.mouse_x, py5.mouse_y, self.circle_radius)


def setup():
    global width_, height_, layout
    py5.size(width_, height_)
    layout = Py5Layout(style=Style(background_color=(255,255,255), width="100%", height="100%"), width=width_, height=height_)

count = 0
def draw():
    py5.no_stroke()
    global count, last_print_time
    count += 1
    with layout:
        CustomSketch(circle_radius=100,
                        circle_color=(255,0,0),
                        style=Style(background_color=(255,255,255),flex=1), width=width_, height=height_)
        with Div(style=Style(background_color="cyan", width="100%", height="50%", justify_content="center", align_items="center", align_content="center", font_size=40), name="div2"):
            Text("Woah look at that circle go!!!!")
py5.run_sketch()
```

**into this**
![custom sketch]([./examples/custom_sketch.gif](https://github.com/TyTodd/py5-layout/blob/c9e807431f98d4d06c19038beb155f72566033dc/examples/custom_sketch.gif))

## [Phone Charging Station Kiosk](https://github.com/TyTodd/charging-station)
[![Watch the video](https://img.youtube.com/vi/dQw4w9WgXcQ/0.jpg)](https://youtu.be/LPlF9MMSO6k)
Touchscreen operated phone charging kiosk I built for my highschool.



<!---
TyTodd/TyTodd is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
- TODO
- add Scribe and BioWallet
--->
