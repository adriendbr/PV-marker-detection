The code provide an image processing algorithm to obtain
robust marker tracking on camera recordings. The image processing is used for human motion estimation during the run-up of pole vaulting.
The goal of the algorithm is to obtain the positions
of the marker centres on the camera image in pixels at every time frame and to follow the
different markers between successive frames. The principle of the algorithm
works as follows. Every single frame is first resized to a width of 1800 Pixels (Px)
and a height of 1012 Px using imutils.resize. The markers that where already detected in the
previous frames are tracked with the Lucas Kanade method. The position
of occluded markers are estimated using a kalman filter. Markers that where
not yet detected, or that failed to be tracked for some reason are recognised based
on colour detection. All these markers positions are stored in a list named
tracking_paths that is constantly updated when new marker positions are found. The
markers that are still not detected are simply indicated manually on the frame with
a mouse click. 
