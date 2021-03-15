# Problem Domain, Objects, and the DOM

## Problem Domain

The understanding the problem domain is the hardest part of programming.
To solve this problem you can do one of two things:

- make the problem domain easier (you need to take a part of the problem and fully understand that part before expanding the problem domain)
- get better at understanding the problem domain (it is best to make sure that you understand the problem both internally and externally before trying to solve it with code)

## Objects

Objects group together a set of variables and function.
In an object, variables and functions take on new names:

- variables is called **property**
- functions become known as **methods**
```
   var hotel = {
   
      name: 'Quay',
      rooms: 40,
      booked: 25,      // properties
      
      checkAvailability: function(){
      return this.room - this.booked;   // method
      }
   }
```

### Accessing an object

To access a property or method you use the name of the object, ".", name of property or method
```
   var.hotelName = hotel.name;  or  var hotelName = hotel['name'] - only for varible
   var roomsFree = hotel.checkAvailability();
```

### Creating objects using literal notation

```
   var elName = document.getElementById('hotelName');
   elName.textContent = hotel.name;
   
   var elRooms = document.getElementById('rooms');
   elRooms.textContent = hotel.checkAvailability();
```

## Document Object Model (DOM)

DOM specifies how browsers should create a model of an HTML page and how JS can access the content of a page.
The DOM neither part of HTML or JS. It is a separateset of rules.
DOM covers two primary areas:

- making a model of the HTML page
- accessing and changing the HTML page

As a browser loads a webpage, it creates a model of the page - **DOM TREE**
Accessing and updating the DOM tree involves two steps:
- locate the node that represents the element you want to work with
- use its text content and atributes

Method that find elements in the DOM tree are called DOM queries.
When you need to use an element more than once, you should use a variable to store the result of this query.

### Selecting an element from Nodelist

There are two ways:

- item() method - return an individual node from the Nodelist
```
   var firstItem = elements.item(0);
```
- array syntax - is preferred the item() method, because it is faster
```
   var firstItem = elements[];
```

You can select elements using: 

- class attributes
- tag name
- CSS selector

   


