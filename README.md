# Youtube-mini

Youtube-mini is a small extension that changes video quality when you change tab on your browser. The point is to prevent unnecessary data consumption both from a user point of view (when you pay your data) and from an environmental point of view (you don't need to get a 4K data flow when you don't look at a video). Of course, when you go back to your Youtube tab or tabs, the quality of the video goes back to its original state.

## Compatibility

For now, this extension only works with Firefox, but we'll try to extend its compatibility to other browsers in the future.

## Method

### The method we use

The simplest method that exists in Javascript : DOM Manipulation. An eventListener is set to know when you change tab. When you do so, a script is launched to manipulate the DOM of your YouTube page to mimic what a user would do to change a Youtube's video quality.

### The method we'd like to use (but it's a lot of work, and maybe out of compliance with Youtube's terms of use)

The video quality data is stored in the local storage of your browser. Simply changing its value doesn't change anything and output errors. Youtube uses a bunch of javascript functions to set this information in the local storage so that it has a real effect on the video's quality without outputing errors, but everything is obfuscated (like, really obfuscated). Finding a way to use Youtube's built-in functions would result in getting an extension without lag. (even if the current lag time is acceptable).
