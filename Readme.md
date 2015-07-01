---
tags: cssi, javascript, jquery
level: 2
languages: javascript
---
# Javascript on the Web
After this lesson, you'll be able to understand:
+ The browser represents html pages with the document object model (DOM)
+ We can use javascript and jQuery to select and modify elements

So far, we have used javascript to do some math and work with some data. Today, we get to use javascript on its home turf - manipulating HTML elements in the browser.

Let’s start with a little example, to give you a taste of the power of javascript before getting into the nitty-gritty of the DOM.

1. Go to https://twitter.com/taylorswift13
2. Open the console
3. Run these two statements, with your name:
```javascript
names = $('.fullname');
names.text('Your Name');
```
BAM! You are a twitter master! How cool are you! So popular!

Now, how did that work?
##The DOM
Your browser keeps all of the elements of the webpage in a tree structure called the Document Object Model. Basically, it keeps track of all of the html elements from the html page, their styles, and the relationships between them - who is nested in who, which elements have which parents and children.
```html
 <body>
  <ul>
    <li>
      <p>Shady Grove</p>
      <p>Aeolian</p>
    </li>
    <li>
      <p>Over the River, Charlie</p>
      <p>Dorian</p>
    </li>
  </ul>
</body>
```
A way to visualize the DOM for that table would be:

![Tree representation of the elements above]()

Javascript can speak the browser’s language - it IS the browser’s language. It is AWESOME for picking elements on a webpage and doing something to them - like picking all the elements on the twitter page and changing them to my name.

Let’s look a little bit more closely at the code we ran to change twitter:

names = $('.fullname');
names.text('Your Name');

First, we are getting all the elements with a particular class, “fullname”, and assigning an array of all of those elements to the variable `names`. Remember, variables store data, and an array is a way to store a list of data. What’s new is the $('.fullname') syntax. .

That syntax is a shorthand way to let us select elements on the page. It lets us use the css selectors that we learned on monday to select elements with javascript. Instead of applying styles to them like we would in CSS, we can change, add, and remove elements on the fly - just like we did in the twitter example.




Once we have all the elements we want, we can update them with another new method - .text(). This method gives us the text inside the element, or updates it if we pass in a new string. It will update the text on all of the elements in our array with the new text - in this case, your name!

Try selecting other html elements on the page and updating their text! What happens?

The selector syntax - $() - and the .text() method actually aren't part of the javascript baked into the browser. They actually come from the jQuery library - a big, commonly used set of useful javascript functions. In order to use this syntax on our pages, we'll need to link up to a javascript library.

PS. While the names of the methods like .text() make sense when you read them, you probably can't figure them out by guessing. Instead, you can look up all the available methods in the online documentation. If you want to do something specific, it’s usually faster to search for it on google, and check for good StackOverflow answers than try to guess the method name yourself.
