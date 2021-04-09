# hw11-UFO-sightings-javascript

#### GRADE: A

After assigning the data from dada.js to a variable, I also assigned the button and form to a variable so I could interact with them in event listeners.

The bulk of the code was within a runEnter() function, which would be executed when the filter button was clicked. First I made sure that the page wouldn't reload while the function was in progress, and I cleared out the tbody tag so each filter would start a fresh table. Then I grabbed each element from the form by specifying the form field by its id and then using .property("value") to extract the user-generated value. 

Because the default for each element was set to blank and the user erasing their element would also set it to blank, I used that as a conditional to determine of the user had entered any text into each form element. If they entered any element, I used .filter() to pick out the rows which matched the user's input. I overwrote the ufoData object in each case to ensure that, if moving through multiple elements, I was working with the object as generated by the previous filters.

After filtering down to data to the user's filters, I used nested forEach() statements to build a new html table from the filtered data. The first forEach generated a new row for every array of data. The second then unpacked each array and appended each piece as its own td tag.

Lastly in runEnter(), I made sure to reset the ufoData object to the original data found it data.js so that each time the button was clicked it would start with the full data.js object, unaffected by the previous filtering. 

To complete the page, I used the .on() function to create event listeners to run the function when the button was pressed. 
