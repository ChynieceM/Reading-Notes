## Video and Audio Content

1. Explain how the ability to use video and audio on the web has evolved since the early 2000s.

-The first influx of videos and audo were made possible by prorpietary plugin based technologies like Flash and Silver light which both had security and accessiblity issues and are now obselete. 
-We now have HTMl solutions and JS APIs for controlling them. 
-The video element allows you to embed a video very easily. 

2. Describe the use of the `src` and `controls` attributes in the `<video>` element.

In the same way as for the img element the src attribute cotnains a path to the video you want to embed. It works in the exact same way. 

Users must be ale to control video and audio playback. This is especially critical for people with epilepsy. You must either use the controls attribute to include the browers own control interface or build you interface using the appropriate JS API. 

3. Why is it important to have fallback content inside the `<video`> element?

The paragraph inside the video tags:
This is called the fallback content this will be displayed if the browser accessing the page doesn't support the video element. This gives your user more options if their browers doesn't support the audio type.

4. Write a very short story where `<audio>` and `<video>` are characters.

Audio in a circus is the deaf guy. Video is the blind guy in a circus. They became best friends and made the best duo in the circus. 

## Grid

1. How does Grid layout differ from Flex?

Flex is one directional; Grid is multi directional. 

2. Grid container, grid item, and grid line are a few important terms to understand when using Grid. Please describe these terms in a few sentences.

Grid container: contains all grid items
Grid item: children elements
Grid line: vertical and horizontal lines that separates elements

## Responsive Images

1. Besides making a site visually appealing across different screen sizes, why should developers make images responsive?

Images dynaically adjust based on what the screen size is; basically how things can scale.

2. Define the following `<img>` attributes `srcset` and `sizes`. Write an example of how they are used.

srcset-you can put in multiple different sources

sizes- extra specifications; defines a set of media conditions and indicates what image size would be best to choose -these are hints and its a condition

3. How is `srcset` more helpful for responsive images than CSS or JavaScript?

It makes hte code more resilient, we dont have to worry about any additonal files loading in or being blocked. 