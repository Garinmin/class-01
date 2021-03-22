# Audio, Video, Images

## Images

Controlling size of images in CSS
```
HTML   
       <img src="images/images1.jpg" 
            class="large" alt="image1">
       <img src="images/images2.jpg" 
            class="small" alt="image2">
            
CSS
       img.large {
           width: 500px;
           height: 500px;
       img.small {
           width: 200px;
           height: 200px;
           }
```

By default, images are inline elements. If you need to put the image on center:
```
   img.large (
      display: block;
      margin: 0 auto;
      }
```
 Background images.
 
 You can place an image behind a HTML element
 ```
    body {
       background- image: url("//http:image.com");
       }
 ```
 When an image is not being repeated, you can use **background-position** property**:
 ```
    background-image: url("image URL");
    background-repeat: no-repeat;
    background-position: center top;   or  (background-position: 50% 50%;)
 ```
 You can use only one value, the second value will default to center.
 You can also use a pair of pixels or percentages. (it means distance from the top left corner.
 The properties must be specified in the following order:
 - background-color
 - background-image
 - background-repeat
 - background-attachment
 - background-position

## Audio, video

Flash is very popular technology used to add animation, video and audio to websites.
If you want to create your own Flash movie, you need to purchase the Flash authoring enveronment from Adobe. 
When you create a Flash file, it is saved with the **.fla** file extention.
You need to export the movie into SWF format(.swf)
To view Flash, the browsers need to use a Flash-plugin.
HTML-5 support ```<video>``` and ```<audio>``` tags and more people are switching to HTML-5.
The ```<video>``` and ```<audio>``` elements allow us to embed video and audio into web pages. 
For example:
```
   <video controls>
      <source src="rabbit320.mp4" type="video/mp4">
      <source src="rabbit320.webm" type="video/webm">
      <p>Your browser doesn't support HTML5 video. Here is a <a href="rabbit320.mp4">link to the video</a> instead.</p>
   </video>
```

