## Object Detection Project
-----
 
### Problem Description 

 - We have a system that produces a stream of frames such that each frame is a solid white background with some 2d objects in the foreground.
 - The stream of successive frames describes the movement of these objects with in the image across time.
 - Here is an example of the kind of images that our system produces.
 - Your task is to write a **"ObjectTracker"** component.
 - Your Object Tracker will expose a single function or method called **"analyze_frame"**.
 - As our system produces frames, each one will passed, one at a time, to your ObjectTracker component through your analyze_frame().
 - `analyze_frame()` will process each new frame-image and return two types of information about the frame.
   
     1. A list of unique identifiers such that each unique identifier corresponds to one unique
object that is visible in the input frame. When a previously unseen object appears on a
frame, it should be assigned a new unique identifier and that identifier should be
returned in the list of unique identifiers returned by `analyze_frame()` and that same
unique identifier should be returned in the array of identifiers for each successive frame
that also contains that object. If/when that object exits the frame, that identifier should no
longer appear in the array returned by `analyze_frame()`.
     2. Information about location of each object. It can either find the centroid location of each
object or find a bounding box that surrounds the object.Please be prepared to walk us through the solution you came up with for this and the various
trade-offs you had to consider when writing your solution and your sense of the limitations and
shortcoming of your solution.
 
### Dataset

Sample data sequence 1:
https://www.dropbox.com/s/dx8f5ng4ui0aroi/sample1.zip?dl=0

Sample data sequence 2:
https://www.dropbox.com/s/njevjwkkhprnfeg/sample2.zip?dl=0