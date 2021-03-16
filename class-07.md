# Object-Oriented Programming, HTML Tables

## Domain Modeling

An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an **object-oriented model**.
To define the same properties between many objects, you can use a constructor function.
```
   var EpicFailVideo = function(epicRating, hasAnimals) {
      this.epicRating = epicRating;
      this.hasAnimals = hasAnimals;
   }

   var parkourFail = new EpicFailVideo(7, false);
   var corgiFail = new EpicFailVideo(4, true);

   console.log(parkourFail);
   console.log(corgiFail);
```
The variable _EpicFailVideo_ is declared and then assigned a function with two parameters called _epicRating_ and _hasAnimals_.

[Domain modeling](https://github.com/codefellows/domain_modeling#domain-modeling)

## Tables

Sometime we need to represent information. in a grid format (financial reports, sport results ...)
Use tables for this. Each block in the grid is reffered to as a table cell.
In HTML a table to create with the ```<table>``` element.
The contents of the table are written out row by row.
Every row starts using ```<tr>``` element.
Each cell of a table represented using a ```<td>``` element. 
The ```<th>``` element is used as the ```<td>``` but it represent the heading for a either a column or a row. Yuo can use the _scope_ attribute to indicate whether it is a heading for column or a row.
```
   <table>
      <tr>
         <th></th>
         <th scope="col">COL1</th>
         <th scope="col">COL2</th>                   
      </tr> 
      <tr>
         <th scope="row">ROW1:></th>                COL1   COL2
         <td>elem1</td>                       ROW1: elem1  elem2
         <td>elem2</td>                       ROW2: elem3  elem4
      </tr>                                        
      <tr>                                    
         <th scope="row">ROW2:></th>          
         <td>elem3</td>
         <td>elem4</td>
      </tr>
   </table>
```
The _colspan_ attribute indicates how many columns that cell should run across.
The _rowspan_ attribute indicates how many rows that cell should run across.
```
   <td colspan="2">Element</td>
   <td rowspan="2">Element</td>
```
The ```<thead>```, ```<tbody>```, ```<tfoot>``` elements help distinguish between the main content of table and the first and last rows.

## Objects

### Creating an object

You can create a new object using a combination:
```
   var hotel = new Object();
   
   hotel.name = 'NAME';
   hotel.rooms = 50;                          PROPERTIES
   hotel.booked = 25;
   
   hotel.checkAvialability = function(){      METHOD
   return this.rooms - this.booked;
   };
```
where:
- hotel -object
- name, rooms, booked, checkAvialability - keys
- NAME, 50, 25, function - value

### Updating an object

To update the value of properties, use dot natation or square brackts:
```
   hotel.name = 'NAME2';
        or
   hotel['name'] = 'NAME2';
   
