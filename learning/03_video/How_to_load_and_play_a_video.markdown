---
.. title: Load and play a video
.. type: howto
---

Select a video to load and play. 

Create a new folder in the bin/data folder of your OF project, name it "movies" and drop your video in it. 

####In the ```ofApp.h``` file: 

Add an instance variable of type ```ofVideoPlayer``` for the video you wish to load.

 	ofVideoPlayer fingerMovie;

####In the ```ofApp.cpp``` file:

In the ```setup``` function:

Load the video by calling the ```load()``` method of ```ofVideoPlayer ```, with the relative path to the video:

	videoName.load("INSERT FILE PATH HERE");
	

Start playing the video:

	videoName.play();

Example:

	void ofApp::setup(){
		fingerMovie.load("movies/fingers.mov");
		fingerMovie.play();
	}
	
	
In your ``update()`` function:


	videoPlayer.update();


Example:

	void ofApp::update(){
		fingerMovie.update();
	}

In your ``draw()`` function:


	videoPlayer.draw(xPosition, yPosition, width, height);


Example:

	void ofApp::draw(){
		fingerMovie.draw(0, 0, 400, 300);
	}
	
###For more information:

take a look at: ```examples/video/videoPlayerExample```
