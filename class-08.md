# CSS Layout

CSS treats each HTML element as own box.
There are:
- block level elements - start a new line (h1, p, ul, li)
- inline elements - flow in between surrounding text (img, b, i)

A box may be nested inside several other block-level elements.
CSS has the following positioning schemes:

- normal flow (default position) Every block element appears on a new line, one after another vertically down the page.
-  relative positioning - the element moves from the normal flow.
-  absolute positioning - this positions the element in relation to its containig element.
-  fixed positioning - this element do not move when the user scrolls up or down the page.
-  floating element - this element becomes a block-level element arround which other content can flow.
-  sticky positioning - this same fixed element, do not move when the user scrolls up or down the page inside the block in which it is located.

When you move any element from normal flow, boxes can overlap. **z-index** allows you to control which box appears on top.

Using float to place elements side-by-side
```
   body{
   width: 750px;}
   
   p{
   width: 230px;
   float: left;}
```
The **clear** property allows you to say that no element should touch the left or right sides of a box.
```
   p{
   clear: left;}
```

Creating multi-column layouts with floats
```
   .column1 {                                 .column1, .column1, .column1 {
      float: left;                               float: left;
      width: 620px;                              width: 300px;
      margin: 10px;}                             margin: 10px;}
   .column2 {                    OR    
      float: left;
      width: 300px;
      margin: 10px;}
   ```
   
There are _fixed width_ and _liquid_ layouts.

In the fixed width usually use width in pixels ``` width: 960px; ```

A liquid layout uses % from screen width ``` width: 90% ```

### Layout grids

Many designers use a grid structure to help them position item on a page. 
Usually use 960 px wide 12 column grid.

### CSS frameworks

You can include the CSS framework code in your projects rather than writing the CSS from scratch. 
For example, the 960.GS grid: ``` <link rel="stylesheet" type="text/css" href="css/960_12_col.css"/> ```
This framework you can find this:
[960.GS Grid](https://960.gs/)

### Multiple style sheets

There are two ways to add Multiple style sheet to a page:

- In HTML you can use a separate ```<link>``` elements
```
   <link rel="stylesheet" type="text/css" href="css/site.css"/>
   <link rel="stylesheet" type="text/css" href="css/tables.css"/>
```
- Your HTML page can link to one style sheet and that stylesheet can use the @import rule to import other style sheets
```
   CSS: @import url("table.css");
        @import url("typography.css");
```
