---
layout: post
title:  "Bachelor thesis: Post mortem"
date:   2015-08-01 12:30:00
short: Managing dependencies can make or break a project
---

It's been a couple of months since we finished our bachelor thesis. Our result
was a system that is scalable in regards of number of cameras connected and the
whole system can be controlled via a website and websockets from another
computer or something like a iPad. The cameras' position was set via intrinsic
and extrinsic calibration via openCV. The user could see the result in a
realtime with about a 10-20 second delay for the calculations. The user could
then accept the result or redo a scan if desired.

##Dependencies
A big problem we had during the process was the management of dependencies in
external libraries. In the end we used: Boost, Libfreenect, PCL, libwebsockets,
OpenCV, linPNG++ and mongoDB drivers.

At the start of the project, I did some research in both git modules and to
handle external libraries with cmake. The most optimal solution would be to have
everyone in the group just be able to download our repository from github and
run cmake and all would run out of the box. I finally realized that it would
take alot of time to get all of this up and running since we were on both Linux
and mac platform and the time would be better spent beginning development of the
actual project.

We eventually got a lot of problems running the project on all computers as the
list of the dependencies grew bigger. We used our Jenkins CI server as a target
platform and any development had to be able to build on the CI server. At the
end of the project we got access to a stationary workspace and to be up and
running on the machine. It took about 2 hours because of the dependencies to get
going with the development. This is also with knowledge on all the quirks with
any external library (like problems with mongodb drivers versions and BSON).

A solution I found later that could have solved some of the problems for us was
Docker. If we were to run a container with all dependencies rolling, we wouldn't
have to make special cases for different platforms.

##Camera positioning
To be able to make a union of data from multiple cameras, we would have to know
the relative orientation between cameras. We used OpenCV and their calibration
functions for this. This worked good, but a problem we got was that we didn't
have a solution to get camera positions if they were facing each other i.e. we
couldn't get the position of the camera behind the subject. In mocap system this
is often solved with using something like a L-frame at the origin. I looked in
to the possibility of using markers for Augmented reality to achieve this, but
I'm afraid there wasn't any time left to get this running.

##Conclusion
All in all, I think we are all happy with the result we accomplished in the
amount of time we were given. We will see if there will be time for anyone to
continue the development of the system to have a result possible to show off at
the exhibition floor of the visualization center C.

