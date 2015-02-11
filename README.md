# Window Reflections Javascript Library
##### A simple library to help you display content/visualisations on our magic projection window

###Purpose
This library will enable certain keybindings that will handle your visualisation being put into full-screen mode and creating and toggling a mask. 

###Usage
To use, simple include the window_display.js file in your HTML page like so...

```HTML
	<script src="/window_display.js"></script>
```

Make sure the file loads before you try and use it in your main Javascript file. If you're using the async tag, things may not work as you expect. To create the key bindings neccessary for our projection screen and API's, you first need to create a new instance of the window_display library. You can do this like this...

```javascript
	var window = new window_display();
```

Next, we call the bind() function on the window object and pass through the two keys that we want to use to trigger behaviour.

```javascript
	var window = new window_display();

	window.bind("f", "m")
```

The first argument for bind() is the key for making your creation go full screen, providing the full screen Js API is available in the browser it's being displayed.

The second argument is the key that will toggle a mask image over your visualisation. This will hide details in certain parts of our window to stop the projection shining through the printed graphics on our window.

###Methods

####bind(FULLSCREEN, MASKTOGGLE)

Pass through any letter from a-z to represent a key that should be pressed to toggle the respective behaviour. We prefer 'f' for fullscreen and 'm' for mask.

####help()

A help dialog will be output to the console when this method is called.


