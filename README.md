# pixelart generator

Original tutorial: https://youtu.be/DfDPJqD3FjI
Original source: https://github.com/AsmrProg-YT/100-days-of-javascript/tree/master/Day%20%2301%20-%20Pixel%20Art%20Generator

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

The main event (pun intended) is `gridButton.addEventListener`. In this part of the code, we are first set the innerHTML of the `container` element to an empty string. We also initiate a counter with a value of `0`.

From there, we have our first loop, which is responsible for creating the rows for our drawing grid. For each row,
we have another loop to create the individual grid cells (which we refer to as `gridCol`).

For each grid cell, we create some additional event listeners. The first one listens for a `down` event and sets the background color for the cell based on whether the user is painting or erasing.

The second event listener listens for a `move` event. That listner first gets the elementId based on where the mouse is. Then it calls a `checker` function. That function grabs all the cells and loops through them to find the cell that matches the one that the mouse is over. The function then sets the background color based on whether the user is drawing or erasing.

The last event listener listens for the `up` event, which tells the code to stop trying to draw or erase anything.

The rest of the event listeners set the values we need to set the grid size, create or remove the grid, and so on. 

I was really amazed at how much logic could go into an event listener. I'm sure we could have moved a lot of this code into separate functions, but I'm not sure that would be absolutely necessary.

I also realize now why, in some drawing tools, if you move the mouse fast enough, the drawing grid doesn't keep up. It's likely code like this can only respond so quickly to what the user is doing. Fine for an application like this, but I can only imagine what professional drawing applications have to deal with!

## Conclusion

These are just my rough notes on my experience. For those of you who know my background as a technical writer, this is not a representation of my work! I just wanted to capture what I experienced and process what the code was doing. If you think I should write a real tutorial on this code, you can always ask me. I'm usually somewhere.