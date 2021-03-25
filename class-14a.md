# CSS Transforms, Transitions, and Animations

## Transforms

The `transform` property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.

### 2D Transforms

Two-dimensional transforms work on the x and y axes, known as horizontal and vertical axes.

#### 2D Rotate

The transform property accepts a handful of different values. The rotate value provides the ability to rotate an element from 0 to 360 degrees. Using a positive value will rotate an element clockwise, and using a negative value will rotate the element counterclockwise. The default point of rotation is the center of the element, 50% 50%, both horizontally and vertically. 
```
HTML

<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>

CSS

.box-1 {
  transform: rotate(20deg);
}
.box-2 {
  transform: rotate(-55deg);
}
```
#### 2D Scale

The default scale value is 1, therefore any value less than 1 makes an element appear smaller while any value greater than or equal to 1.01 makes an element appear larger.
```
.box-1 {
  transform: scale(.75);
}
.box-2 {
  transform: scale(1.25);
}
```
It is possible to scale only the height or width of an element using the scaleX and scaleY values.

Also there are **2D Translate** and **2D Skew**

### 3D Transforms

#### 3D Rotate

With three-dimensional transforms we can rotate an element around any axes.
```
.box-1 {
  transform: perspective(200px) rotateX(45deg);
}
.box-2 {
  transform: perspective(200px) rotateY(45deg);
}
.box-3 {
  transform: perspective(200px) rotateZ(45deg);
}
 ```
 Also there are:
 
 - 3D Scale
 - 3D Translate
 - 3D Skew

[Transforms](https://learn.shayhowe.com/advanced-html-css/css-transforms/)

## Transitions

There are four transition:

- transition-property
- transition-duration
- transition-timing-function
- transition-delay

In the example below the box will change its background color over the course of 1 second in a linear fashion.
```
.box {
  background: #2db34a;
  transition-property: background;
  transition-duration: 1s;
  transition-timing-function: linear;
}
.box:hover {
  background: #ff7b29;
}
```

## Animations

To set multiple points at which an element should undergo a transition, use the @keyframes rule. The @keyframes rule includes the animation name, any animation breakpoints, and the properties intended to be animated.
```
@keyframes slide {
  0% {
    left: 0;
    top: 0;
  }
  50% {
    left: 244px;
    top: 100px;
  }
  100% {
    left: 488px;
    top: 0;
  }
}
```
[Transitions & Animations](https://learn.shayhowe.com/advanced-html-css/transitions-animations/)

[8 SIMPLE CSS3 TRANSITIONS](http://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users)
