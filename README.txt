~ explanation
- child

* Tried to take out a lot of the stuff/files that are not relevant
* Also some of the links are in absolute form, so it'll go to the actual lifelens.ca site instead of locally


root/
 - profile.html
	~ the demo vertical page
 - demo/
	~ contains CSS (css/) and JS (js/) for horizontal page, images (images/ Ontario Science Centre/), profile.html CSS and JS (profile/)
	- index.html
		~ the demo horizontal page
 - events/
	~ the interactive demo
	- demo.html
		~ get event name
	- upload.html
		~ using an external JS + upload.php for the drag and drop upload
		~ gets the event name and creates the folder
	- uploads/
		~ all the events: folders that contain the images (folder name = event name)
	- profile.html
		~ the profile page for the interactive demo
		~ reads the uploads/ folder using php, creates an event for each folder
		~ on click, send a variable to demo/index.html the event name (aka folder name from uploads)
		~ it'll ignore folders that are empty
	- demo/
		~ just like the root folder demo/ with different index.html, and css
		- index.html
			~ reads the variable (aka folder name from uploads) and creates an event by reading exif data of all the images inside
