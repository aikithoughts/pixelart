# pixelart generator

Original tutorial: 
Original source:

In this tutorial, I followed along while the developer created a nice little pixelart generator. As a novice developer, here are some of my observations:

## HTML and CSS are powerful

The first half of the tutorial has almost no JavaScript whatsoever. It's all setting things up in HTML and CSS. I was particulary taken with the line:

`<input type="color" id="color-input">`

This is the HTML that creates the color picker in the generator. And it just...does it! Realizing that tools like this remind me that all platforms, languages, and what-have-you contain significant tools to help you get your work done.
Part of your responsibility as a creator is to know your tools so you can leverage them effectively. After all, if you were a chef, you *could* make your own pasta, but if that's the point, you could also just *buy* it.

I was also impressed with the `range` input type, which creates a slider. That was pretty interesting too.

## Checking for device types

This code example is also the first one I've done where the code checks for the device type. It looks like this check exists so the code can use the correct events for detecting when the user is drawing or erasing.
I'll keep this pattern in mind for future efforts; it seems like a convenient way to write code efficiently.

## Event listeners

The main event (pun intended) is `gridButton.addEventListener`. In this part of the code, we are 