# cctv-motion-canvas-clip-region
Using canvas region clipping with diffcam to detect motion.

```
This code uses my own modified version of Diffcam and socket.io / rtsp library 
I have not included that code here.
This post is merely to show how to use canvas clipping with motion detection
```

Going beyond rectangles for motion detection using Diffcam (https://github.com/lonekorean/diff-cam-engine)

My original motion detection was limited to boxes

![Interface](https://github.com/wilwad/cctv-motion-canvas-clip-region/blob/master/ui/1.png)

Our clipping region editor

![Interface](https://github.com/wilwad/cctv-motion-canvas-clip-region/blob/master/ui/2a.png)

We dynamically create the inputs to edit the X-Y coordinates from a points file points.js using our camera as key (109)

![Interface](https://github.com/wilwad/cctv-motion-canvas-clip-region/blob/master/ui/points.png)

How we clip the canvas to the points

![Interface](https://github.com/wilwad/cctv-motion-canvas-clip-region/blob/master/ui/diff-clip.png)

The clipped canvas passed to Diffcam

![Interface](https://github.com/wilwad/cctv-motion-canvas-clip-region/blob/master/ui/0.png)

DiffCam will do its thing and give us a motion box as usual.
We will draw the bounding box over our CCTV canvas and also overlay the clipping points over it.

![Interface](https://github.com/wilwad/cctv-motion-canvas-clip-region/blob/master/ui/diffcam.png)

Final output, looks much better 

![Interface](https://github.com/wilwad/cctv-motion-canvas-clip-region/blob/master/ui/0a.png)

Our CCTV motion detection with canvas clipping (Day)

![Interface](https://github.com/wilwad/cctv-motion-canvas-clip-region/blob/master/ui/3.png)

Our CCTV motion detection with canvas clipping (Night)

![Interface](https://github.com/wilwad/cctv-motion-canvas-clip-region/blob/master/ui/4.png)
