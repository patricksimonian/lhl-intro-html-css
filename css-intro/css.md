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
 
 Edit the styles.css file you just created and add this code to it. 
 ```
    body {
      font-family: 'Lato', 'sans-serif';
      font-size: 18px;
    }
 ```
like so...
![first selector](/assets/imgs/step-18.png)
make sure to save the file!

what we are doing is adding some very basic styles like what the font is and how large it is going to be. These styles will flow (cascade) down to all our HTML elements because we targeted the body.

## Step 2

In order to use those styles we just wrote we need to link the styles.css file to the index.html file. 

In your index.html file, modify the ```<head>``` tag and copy and paste these two tags inside..
```
  <link rel="stylesheet" type="text/css" href="./public/styles/styles.css">
  <link href="https://fonts.googleapis.com/css?family=Lato|Raleway:300,400" rel="stylesheet">
```

It should look like this
![first selector](/assets/imgs/step-19-new.png)
make sure to save the file!

The lower link tag is linking to an external stylesheet over the internet. This one is specifcally for getting some neat fonts (from Google) to use on our page. Leveraging other peoples' resources (code, fonts, images) is a very common practice in web development. 

If everything went well, when you refresh your browser and view your website you should notice the font is different!.

We are getting there..

## Step 3

Let's modify our existing HTML (in index.html) and add some class and id attributes to the elements so that
we can more <i>specifically</i> style them. 
  
Take your time with this as there are many HTML attributes that were added. They will be summarized below the picture.

![adding-selectors](/assets/imgs/step-20-new.png)

 #### Summary of all the HTML changes
 -the main ```<header>``` tag had an id attribute of "main-title" added. 
 
 -the ```<img>``` tag inside the main header had an id of "profile-thumbnail" added
 
 -the first```<section>``` tag has an id of "main-profile-container"
 
 -the ```<section>``` tag inside the first section has an id of "main-descriptions" and a class of "information-block"
 -the ```<h2>``` inside the main descriptions section  has an id of "about-me-header"
 
 -the ```<article>``` inside the section has an id of "alt-descriptions" and a class of "information-block" 
    (this is because we may add more articles if needed)
    
 -the ```<ul>``` tag has a class of "list-group"
 
 -the ```<footer>``` tag at the bottom of the index.html has an id of "page-bottom"
 
 -the ```<a>``` tag inside the footer has a class of "social-links"
 
  ## Step 4
   
Perfect! We have a whole bunch of elements, classes and ids that we can target with our CSS and get styling. 

Copy and Paste this code inside your "styles.css" file replacing whatever was inside there earlier. 

```
body {
  font-family: 'Lato', 'sans-serif';
  font-size: 18px;
}
/*these comma seperated selectors is a shortcut to apply the same set of style to these
three elements*/
h1, h2, h3 {

}

aside {

}

hr {

}

main {

}

.list-group {
  
}

/*joining selectors like this is just like saying target all of the <li> tags found within
the element(s) that have the list-group class*/
.list-group li {

}

.information-block {
  
}

.personal-descriptions {
  
}

.social-links {

}

.social-links:hover {

}

#about-me-header {

}

#alt-descriptions {

}

#main-profile-container {

}

#main-descriptions {

}

#main-title {

}

#main-title h1 {

}

#page-bottom {

}

#profile-thumbnail {

}
```

Let's begin by fixing our profile image so that it looks like the thumbnail icon we saw in the final result.

add this css code inside the #profile-thumbnail selector
```
#profile-thumbnail {
  width: 150px;
  height: 150px;
  border-radius: 50%;
 }
```
Look at these css properties and try to figuire what's going on, play with the border-radius, width and height then save and refresh the page. What happens? The best way of knowing how all these different styling rules work is by experimenting.

this is my end result..

![changed profile pic](/assets/imgs/part-21.png)

## Step 5

 There are many different properties to use when styling with css and we encourage experimenting with colors, background-colors, height, width and so on. Besides changing <i>how</i> and element looks we can also change its position on the page with several different properties. 
 
 Before we can get into that we need to go over the <strong>box model</strong>
 
 ##### CSS Box Model
 
 ![box model](/assets/imgs/part-22.png)
 
 We can position the content inside a tag by applying styling rules to an elements margin, border, or padding.
 
 Things to note are:
 
 -margin: pushes the element away from other elements on the page, we often use this to space elements apart from each other
 
 -border: applies a border to an element
 
 -padding: adds 'cushion' around the content of an element. This would increase the distance between an element and its border. 
 
 Now that we have some basic positioning knowledge, let's center our header so it's similar to the final result picture that was demonstrated at the beginning of the workshop. 
 
 Add this code to your #main-title selector so that it looks like this
 
 ```
 #main-title {
  margin: 45px auto 25px;
  text-align: center;
  width: 400px;
}
```

Again experiment around with the values there and add your own CSS properties. 
The numbers following the margin may look funny but it's short hand notation. 
You can learn more about the short hand properties <a href="https://www.w3schools.com/css/css_margin.asp"> here.</a>


