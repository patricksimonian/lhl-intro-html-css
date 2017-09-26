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
