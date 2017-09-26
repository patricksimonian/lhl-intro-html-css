#HTML

So as we discussed in the lecture, HTML stands for Hyper-Text-Markup-Language.
What this really means is that HTML is the language the provides content to a website.
Every word we read, every image we see, every link, or text or password field is created with HTML. 

**one thing to emphasize is that browsers provide some default styling (CSS) to our HTML**
 
 For example, it does things like spaces out paragraph tags. 
 
```
  <p>I'm a paragraph</p>
  <p>I'm another paragraph</p>
```
will look like:
  <p>I'm a paragraph</p>
  <p>I'm another paragraph</p>

It will also change the font size and font weight of header tags.

```
  <h1>Oh hey there</h1>
  <h2>Oh hey there</h2>
  <h3>Oh hey there</h3>
```
will look like:
  <h1>Oh hey there</h1>
  <h2>Oh hey there</h2>
  <h3>Oh hey there</h3>

What's the importance of this? To just realise that when it comes to HTML, all we 
really should care about is what the <strong>content</strong> is and <em>not</em> how it looks!

Okay there's my sermon.. let's get started. 

## Step 1
  First things first, we will need an html file to call home in order to start coding. 
  Do this by creating a file called <b>"index.html"</b> inside of your project folder. 
  
  ![make new file](/assets/imgs/tutorial-step-8.png)
  
  You project directory in your code editor should look something like this. 
  
  ![directory with index.html](/assets/imgs/tutorial-step-9.png)

## Step 2

Open the file and add the following html code into it.

```html
<h1>hello, world</h1>
```
It should look like this.

![hello, world](/assets/imgs/tutorial-step-10.png)

Save the file and then navigate to your project folder and choose to open the **index.html** file in your Web browser. You'll get something like this.

![Hello, Chrome](/assets/imgs/tutorial-step-11.png)

And that's it &mdash; you just built a Web page!

## Step 3
 Okay, most web pages don't just say hello world, and if we are going to get towards our personal profile page we are going to need more content.
 To start off with we will rewrite our index.html to look like this. 
 
 ![basic html skeleton](/assets/imgs/tutorial-step-12.png)
 
 ## Step 4
 
 Perfect, we have a working skeleton to start our markup. 
    
 Before we start coding our HTML in it's best to visualize how our content is going to live in the page. 
 
 The best way to do that is to start thinking <b>boxes</b>. 
    
![thinking boxy](/assets/imgs/step-13.png)
    
 This is because every element/tag in HTML can be thought of as living in its own box. 
Elements/tags can be placed inside other boxes (other elements). We call that process nesting. 
    
 The image above visualizes how all our HTML elements will live and how they are oriented/nested. 
    
***One important thing to realize is although this is how we visualize our content, 
IT WILL NOT LOOK LIKE THIS when we load the website**
    
This is because we are simply constructing the foundation of how all the HTML works together. For it to look how it is shown in the image above, we will style it with CSS later in the tutorial. 
 
For now let's finish off writing our foundation HTML. Here's the snippet of code to follow. 

![finished skeleton](/assets/imgs/step-14.png)
  
## Step 5 - Filling In Some Content

Fill in your foundation HTML Code with whatever you like,
I used my HTML to make a personal profile page but you could do anything, even make a page about one of your favourite animals/activities.

Here's what my code looks like 

```
<!DOCTYPE html>
<html>
<head>
  <title>My Personal Page | Home</title>
</head>
<body>
  <!-- a navigation bar which may or may not be needed depending on how large your website is -->
  <nav></nav>
  <!-- the main content of your page -->
  <main>
    <!-- the title-->
    <header>
      <!-- online image link, copied from url. Trying searching google images for a link -->
      <img src="https://scontent-sea1-1.xx.fbcdn.net/v/t1.0-9/307211_10151225912177690_682126725_n.jpg?oh=2987474d903096b0dfa3d9fec9977bf3&oe=5A4A5DDA" alt="my profile pic">
      <h1>My Profile Page</h1>
    </header>
  
    <!-- main section  -->
    <section>
      <!-- title for main section -->
      <h2>About Me</h2>
      <!-- a small article about myself -->
      <article>
        <p>My Name is Patrick Simonian. I'm a Full Stack web developer and instructor.</p>
      </article>
    </section>
    <!-- here's an aside of more things that are related to the section above -->
    <aside>
      <h3>Some of my favourite things are:</h3>
      <ul>
        <li>Pizza</li>
        <li>Traveling</li>
        <li>Cycling</li>
        <li>Rock Climbing</li>
        <li>Hiking</li>
      </ul>
    </aside>
    <!-- links to some social things such as my github profile -->
    <footer>
      <a href="https://github.com/patricksimonian">My Github Projects</a>
    </footer>
  </main>
</body>
</html>
```
You probably noticed this funny syntax..
*** ```<!--  -->```  what's that all about?***

Those are HTML comments, this allows us to code in messages for ourselves or other developers that won't show up on the website but is visible in the HTML files. 

After everything is said and done this is what the final result should more or less look like. 
![result](/assets/imgs/step-15.png)

Like mentioned earlier, the way everything is positioned doesn't exactly look like our box schematic from above but that's because it hasn't been styled yet.

Speaking of style. Let's dive right into CSS with the <a href="https://github.com/patricksimonian/lhl-intro-html-css/edit/master/css-intro/css.md">next tutorial</a>.

