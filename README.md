Screen Capture for Alfred
============

An few simple terminal commands so you can take screen shots from [Alfred App](http://alfredapp.com/) and edit them in Privew. You will need Alfred and the Powerpack to use this.

Installation
----------------

To install Screen Capture in Alfred **double click on the extension file**.

How to use
----------------

######Once installed with Alfred you can run the following commands


    snap fs   ::  Take a screen shot of your full screen
    snap w    ::  Take a screen shot of any open window
    snap s    ::  Take a screen shot of a selection of your screen
      

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
		open -a "Adobe Photoshop CS6" ~/Desktop/fullscreen-snap.png	elif [ $response == "w" ]
	then
		screencapture -ic ~/Desktop/window-snap.png
		echo "Snap Saved to your Desktop"
		open -a "Adobe Photoshop CS6" ~/Desktop/window-snap.png	elif [ $response == "s" ]
	then
		screencapture -ic ~/Desktop/selection-snap.png
		echo "Snap Saved to your Desktop"
		open -a "Adobe Photoshop CS6" ~/Desktop/selection-snap.png
	else
		echo "Query must be: fs (fullscreen), w (window) or s (selection)."
	fi


Download and Help
----------------
Direct Download &#x2192; [Screen Capture](http://rnydm.us/Lfs0) 

Helpful Files &#x2192; [Screen Capture Help](dev.rainydaymedia.net/alfred)
    