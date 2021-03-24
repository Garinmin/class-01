# Local Storage

What is HTML5 Storage? Simply put, it’s a way for web pages to store named key/value pairs locally, within the client web browser.
Like cookies, this data persists even after you navigate away from the web site, close your browser tab, exit your browser, or what have you. Unlike cookies, this data is never transmitted to the remote web server.
Like other JavaScript objects, you can treat the _localStorage_ object as an associative array.
```
   var foo = localStorage["bar"];
   // ...
   localStorage["bar"] = foo;
```
There are also methods for removing the value for a given named key, and clearing the entire storage area (that is, deleting all the keys and values at once).
```
   interface Storage {
   deleter void removeItem(in DOMString key);
   void clear();
   };
```

## LIMITATIONS IN CURRENT BROWSERS

5 megabytes is storage space each origin gets by default.
“QUOTA_EXCEEDED_ERR” is the exception that will get thrown if you exceed your storage quota of 5 megabytes.
One thing to keep in mind is that you’re storing strings, not data in its original format.

## HTML5 STORAGE IN ACTION

Let’s see HTML5 Storage in action.
If you close the browser window mid-game, you’ll lose your progress. But with HTML5 Storage, we can save the progress locally, within the browser itself. 
