Screen Capture and Edit for Alfred / Alfred 2
============
> Updated for Alfred 2 workflows

Created this little productivity saver to help write documentation. I'm not a fan of having an app just sitting in the menu bar... not to mention most of the features are built right into the OS. 

All this workflow is just a list of a few simple terminal commands so you can take screen capture/shot from [Alfred](http://alfredapp.com/) and edit them in Preview. 

######Requirments:
 1. [Alfred](http://www.alfredapp.com/#download) (free)
 2. [Powerpack](http://www.alfredapp.com/powerpack/) (£17)


Installation
----------------

To install in Alfred ***double click on the extension file***.  
Tp install in Alfred 2 ***double click on the workflow file***.

How to use
----------------

######Alfred 1


    snap fs   ::  Take a screen shot of your full screen
    snap w    ::  Take a screen shot of any open window
    snap s    ::  Take a screen shot of a selection of your screen

######Alfred 2

![Alfred screenshot 2]()  
select the action you want to do... and hit Enter

*If you're doing a time screen capture you'll need to set the length in seconds*

>A few things new in Alfred 2 to keep in mind:  
**Currently have the file names set to the date and time ** 

Edit Default Image App
----------------
######Change the following on all three commands:
	
	screencapture -icP ~/Desktop/selection-snap.png
	echo "Snap Saved to your Desktop"

######Add the following values:
	
		screencapture -ic  ~/YOUR NEW FOLDER PATH/custom_file_name.extensionType
		echo "Snap Saved to your YOUR NEW FOLDER PATH"
		open -a YOUR APPLICATION NAME ~/YOUR NEW FOLDER PATH/custom_file_name.extensionType

    
Example
----------------
*If you want to save to your Desktop and Edit in Photoshop*
	
	response="{query}"
	if [ $response == "fs" ]
	then
		screencapture -ic ~/Desktop/fullscreen-snap.png
		echo "Snap Saved to your Desktop"
		open -a "Adobe Photoshop CS6" ~/Desktop/fullscreen-snap.png	
	elif [ $response == "w" ]
	then
		screencapture -ic ~/Desktop/window-snap.png
		echo "Snap Saved to your Desktop"
		open -a "Adobe Photoshop CS6" ~/Desktop/window-snap.png	
	elif [ $response == "s" ]
	then
		screencapture -ic ~/Desktop/selection-snap.png
		echo "Snap Saved to your Desktop"
		open -a "Adobe Photoshop CS6" ~/Desktop/selection-snap.png
	else
		echo "Query must be: fs (fullscreen), w (window) or s (selection)."
	fi


Download and Help
----------------
Direct Download &#x2192; [Screen Capture](http://i.makitra.in/Ndbp)   
Alfred Forums &#x2192; [comment on the topic](http://www.alfredforum.com/topic/1118-screen-shot-with-aflred/)

    