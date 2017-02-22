FINDING LANE LINES ON THE ROAD

The goals / steps of this project are the following:

-Make a pipeline that finds lane lines on the road

-Reflect on your work in a written report

-Reflection


DESCRIBE YOUR PIPELINE. AS PART OF THE DESCRIPTION, EXPLAIN HOW YOU MODIFIED THE DRAW_LINES() FUNCTION.

The pipeline function will transform the video below:

![Alt text](solidYellowLeft_INPUTVIDEO.jpg?raw=true "Input Video")

Into a video that highlights the left/right guidelines using 8 steps:

![Alt text](solidYellowLeft_OUTPUTVIDEO.jpg?raw=true "Output Video - With Lines Added Using Pipeline")

The pipeline function consisted of 8 steps:

Step1-convert image to grayscale

Step2-gaussian blur of the grayscale image

Step3-canny edge detector of the Gaussian image

Step4-get the size of the image in pixels

Step5-based on the image size , create vertices using the lower corners and for the upper corners used 55% of the vertical direction and 49/51% of the horizontal direction.

Step6-hough lines transform which uses the draw_lines function

-The draw_lines function does the following:

	-separates positive and negative slope lines
  
	-creates a single line for the positive slope lines by using an average slope
  
	-creates a single line for the negative slope lines by using an average slope
  
Step7-weighted image – combines the original image with the lines


IDENTIFY POTENTIAL SHORTCOMINGS WITH YOUR CURRENT PIPELINE


-A very curvy road would be difficult to process, since the canny edge algorithm uses straight lines.

-A car in front could be blocking the road and there would be no lines.

-The camera lens could make straight lines appear curvy due to optical issues.



SUGGEST POSSIBLE IMPROVEMENTS TO YOUR PIPELINE


-Instead of using a straight line function a 2nd order curve could be used for when the car follows a curved road.

-Camera lens distortion can be fixed by using libraries that correct using a sensor/lens database (such as what is used in photoshop).

