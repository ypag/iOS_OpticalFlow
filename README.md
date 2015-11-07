**Summary:**
I plan to efficiently implement optical flow on iOS platform. Aim of the project is to track motion of swings at playgrounds to teach children(age 8-12) concept of periodic motion and show comparative analysis with linear motions observed at playgrounds. 

**Background:**
I plan to take advantage of computational speedups available to iOS device - For example I plan to make use of inverse composition in the LK algorithm to implement real time optical flow on iOS device. In Inverse composition algorithm, Jacobian Matrix is precomputed and there is no need to solve a system of linear system similar to classical LK additive method, which makes the algorithm computationally efficient. 

**The Challenge:**
OpenCV hascalcOpticalFlowPyrLK method to perform optical flows. Brad Larson’s GPUImage library has a built in GPUImageMotionDetector. This motion detector does frame to frame comparisons based on low pass filter and can identify number of pixels that have changed. It does not do feature matching or optical flow. Aim of the project is to find efficient ways of doing real time optical flow on iOS. 

**Goals and Deliverables:**
- I plan to create a robust tracking algorithm to detect and analyse motions at a playground , specifically at swings and build a game around this idea to teach children about physics of motions -linear and periodic. 
- I hope to achieve motion based augmented reality. Based on swing’s relative velocity or consistency of pumping the swing would render a 3d object in space 
- For evaluation : I am planning to take snapshots of app working and also record a video of the app in action
It seems possible to achieve (1) within the given timeframe of the project

**Schedule:**
* Week1 : Implement calcOpticalFlowPyrLK with opencv and try MotionDetector class within GPUImage framework, analyse results and find painpoints. Implement facetracking and eye tracking on real time video. Calculate varying size of face and distance between eyes as object person closer and further from camera - can this be used to estimate motion of a child on a swing? 
* Week2 : Get raw data from tracking, Understand current performance,analyse and Improve performance (Inverse LK implementation)
* Week3 : Use raw data to build analytics, Create Storyboard, User Interface  and visualisations to show user the feedback
* Week4 : Render 2d/3d objects based on motion analysis. Create interaction between rendered object and user actions : For example, tapping on the rendered object would make it vanish ( In the game these would be game assets such as game currency that a player would tap and collect) 


