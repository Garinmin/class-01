# Readings : HTML Lists, Control Flow with JS, and the CSS Box Model

## HTML

### Ordered lists

The ordered lists is created with **ol** element

Each element in the list is placed between **li** elements

```<ol>
       <li> any text </li>
       <li> any text </li>
   </ol>
```

### Unordered list

Use **ul** and **li** elements

### Definition lists

Use **dl**, **dt** and **dd** elements

```
   <dl>
      <dt> ... </dt>
      <dd> ... </dd>
      <dd> ... </dd>
      <dt> ... </dt>
      <dd> ... </dd>
   </dl>
```
## CSS

Box dimensions: _width, height_

Limiting width and height: _min-width, max-width, min-height_

Overflow

**hidden** - this property simply hides any extra content that doesn't fit in the box

**scroll** - adds a scrollbar to the box that user can scroll to see the missing content

```
   p.one {
      overflow: hidden;}
   p.two {
      overflow: scroll;}
```

### Border, Margin and Padding

```
border: 2px solid red;
margin: 5px 10px 15px 20px; //top, right, bottom, left
```
You can make the border with a radius

```
   border-radius:100px;
   border-top-left-radius:80px  50px
```

Use _inline, block and inline-block elements_

Change the type with **display** 

You can hide boxes from users with **visibility** property

The visibility can take two values:

- hidden - hides the element
- visible - shows the element

## JS

### Arrays

An array stores a list of values

```
   var colors;
   colors = ['white', 'red', 'green'];
      or
   var colors = new Array('white', 'red', 'green'); // array constructor
```

Index values start at 0

### Loops

- for -loops
```
   for (i=0; i<10;    i++) {cod}
``` 
- while loops
```
   var i=1;
   while (i<10) {
   cod; i++;}
```
- do while loops
```
var i=1;
do {
   cod; i++;
} while (i<1);
```
   



