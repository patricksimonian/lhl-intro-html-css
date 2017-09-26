# CSS

CSS stands for Cascading Style Sheets. It's how we change the look and feel of our HTML markup.

A CSS Rule consists of selector, a property and a value. It looks like this:
```
selector {
    property: value;
}
```
- selector is the element we want to style (such as h1 or li)
- property is one aspect of the element we want to change (color)
- value is the value of that property (such as red) - Remember - the value must have a semicolon ; at the end

Our browsers come with some basic styling for elements, but we usually want to override these with our own styles. 
To do this, we create a .css file and link it in the <head> of our HTML file like this:

```
<head>
    <link rel=”stylesheet” href=”styles.css”>
</head>
```

There are a few different ways we can select or target an element to style it.

You can target all of an element like so.
```
 p: {
   color: red;
 }
```

This would target ***all*** paragraph tags on that page and change their text colour to red.

Sometimes this type of styling can be a little to generic so we add some attributes to our HTML to style our 
elements more specifically.

```
 given this html.. 
  <h1 id="title">Baking Instructions</h1>
  <p id="description"> In order to start baking you'll need these things first..</p>
  <ul>
    <li class="baking-list">An Oven</li>
    <li class="baking-list">A Baking Pan</li>
    <li class="baking-list">And a Good Attitude</li>
  </ul>
  
  we can target specific elements or groups of elements with other selectors like so
  
  targeting by an elements id..
  #title {
    font-weight: bold;
    font-size: 24px;
    border-bottom: 1px solid grey;
  }
  
  targeting a group of elements by a class
  
  .baking-list {
    margin: 4px;
    border: 1px solid #grey;
    padding: 3px;
    background-color: #fafafa;
    color: #6e6e6e;
   }
```

***an important thing to note is that ID's must be unique on a page and that two elements may not have the same ID. 
 Classes can be used as many times as you like however.***
 
 ---
 ## Step 1

 Let's create a css file and place it in our styles directory we made earlier in the project. After that
 we are going to link the css file to our html using a link tag. 
 
 Let's call the file "styles.css"
 
 ![create file](/assets/imgs/step-16.png)
 In the end it should look something like this.
 ![final result](/assets/imgs/step-17.png)
 
 ## Step 2
