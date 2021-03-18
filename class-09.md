# Forms and JS Events

## Forms

There are several types of form controls that you can use to collect information from visitors:

- adding text
- making choice
- submiting forms
- uploading files

How forms work?

1. User submits the information
2. The name of each form control is sent to the server along with the value the user enters or celects
3. The server processes the information
4. The server creates a new page to send back to the browser

### Form structure
```
   <form action="http://www.example.com" method="get">
      <p>TEXT</p>
   </form>
```

### Text input
```
   <form action="http://www.example.com" method="get">
      <p>Username:
            <input type="text" name="username" size="15"
               maxlength="30" />
      </p>
   </form>
```
### Password input
```
   <form action="http://www.example.com" method="get">
      <p>Username:
            <input type="text" name="username" size="15"
               maxlength="30" />
      </p>
      <p>Password:
         <input type="password" name="password" size="15"
               maxlength="30" />
      </p>
   </form>
```
### Text arrea
```
   <form action="http://www.example.com" method="get">
      <p>What did you think og this gig?</p>
      <textarea name="comments" cols="20" rows="4">
         Enter your comments...</textarea>
   </form>
```
## Forms in CSS

There are several CSS properties that were created to work with specific types of HTML elements

- lists
- tables
- forms

Examle CSS aligning form control
```
   div {
        border: 1px solid red;
        margin; 10px;
        width; 200px;}
  .title {
        float: left;
        width: 100px;
        text-align: left;}
```
## Events

Any events can be used to trigger a function in JS:

- UI events (load, error, resize, scroll)
- Keyboard events (keyup, keydown)
- Mouse events (click, mousedown, mouseout)

### How events trigger JS code

1. select the element nodes you want the script respond to
2. indicate which event will trigger the responce
3. state the code you want to run when the event occurs

There are three ways to bind an event

1. HTML event handlers
2. traditional DOM event
3. using DOM event


