# PharoByExample150

By the book , captain - spock - the wrath of khan - star trek.

Lets get started .

This is a very simple introduction to Pharo smalltalk , what you learn here is applicable to every Smalltalk.

To install pharo - you can download and run the launcher 

![The launcher](docs/Chapters/Chapter1/figures/pharo-launcher-2026-05-23_20-07.png)

click new for a new image

![The launcher](docs/Chapters/Chapter1/figures/launcher- click-the-new-image-button-2026-05-23_23-12.png)

now click create image

![The launcher](docs/Chapters/Chapter1/figures/pharo-launcher-step2-2026-05-23_20-08.png)

pharo-launcher-step2-2026-05-23_20-08.png

If you managed to download and install pharo successfully you will be greeted with a window that looks something like this

![Start of Pharo](docs/Chapters/Chapter1/figures/pharo-welcome-14-2026-05-23_20-11.png)

This is the welcome screen of Pharo 

As a beginner you will want to start with the Playground.

You can open a playground by pressing Ctrl + O + P .

Holding down the 'Control key' - your keyboard may have a key that says 'Ctrl' . 

While keeping the 'Control key' pressed down , press and *release* the letter 'O' key - O for Oranges , now press and *release* the letter 'P' key - P for Peter .

you should hopefully see something like this , it will say Playground on the title of the window

![Empty Playground](docs/Chapters/Chapter1/figures/empty-playground-2026-05-23_22-49.png)

Lets type a quick program into the playground

```
'Hello' reverse. 
```

In Smalltalk something surrounded by single quotes is interpreted as a String.

We are sending the message 'reverse' to the string 'Hello' .


![Playground](docs/Chapters/Chapter1/figures/playground-step1-2026-05-23_20-32.png)

Inside the playground I have written a small program , you can type this is in as well 



![Single quote character](docs/Chapters/Chapter1/figures/single-quote.jpg)


To run this program can press the do it all button ![Do it all button](docs/Chapters/Chapter1/figures/do-it-all-icon-2026-05-23_21-07.png)

you will see an Inspector open up 

The inspector allows us access inside the result that we got handed back.

In this case the letters of Hello reversed or rather olleH .

![Inspector](docs/Chapters/Chapter1/figures/playground-step2-2026-05-23_20-32.png)

To recap - we have opened a Playground , wrote a simple program , run the program , got the result

![Inspector](docs/Chapters/Chapter1/figures/playground-step2-2026-05-23_20-32.png)

The Playground is split into two regions 

We have a main coding area initially 

![playground area](docs/Chapters/Chapter1/figures/initial-playground-area-2026-05-23_22-12.png)

and inspector regions which themselves have a mini playground at the bottom

![Inspector area](docs/Chapters/Chapter1/figures/this-is-the-inspector-region-2026-05-23_22-07.png)

the mini playground at the bottom is in context of the result above 

given a different result - the context will be different.





# Appendix 

Some essential morph code to load images from local disk and internet urls , some text and circles ,
makes highlighting and explaining what is going on a lot easier to the reader.

![Essential morphs](docs/Chapters/Chapter1/figures/appendix-helpful-morphs-2026-05-23_22-59.png)


```
handForm := ImageReadWriter formFromFileNamed: '/home/terry/code/PharoByExample150/docs/Chapters/Chapter1/figures/hand-pointer-icon.png'.
pointer := ImageMorph new form: handForm; openInWorld; yourself.


handForm := ImageReadWriter formFromFileNamed: '/home/terry/code/PharoByExample150/docs/Chapters/Chapter1/figures/pharo-launcher-2026-05-23_20-07.png'.
pointer := ImageMorph new form: handForm; openInWorld; yourself.


"Load an image from a URL and create an ImageMorph"
handImage := ZnEasy getPng: 'https://images.icon-icons.com/1464/PNG/512/pointinghand_100160.png'.
pointer := ImageMorph new form: handImage; openInWorld; yourself.

"Move it programmatically"
pointer position: 300@300.

circle := CircleMorph new openInWorld ; color: (Color white alpha: 0.0) ; borderWidth: 5 ; borderColor: (Color green) ; extent: 300@300 ; yourself.

"Create a TextMorph with explanatory text"
indicator := TextMorph new.
indicator contents: 'This is the inspector region';
    color: Color yellow;
    borderWidth: 3;
    borderColor: Color black;
    extent: 200@40;
    position: 100@100;
    openInWorld.


"change text , foreground and background colours"
indicator color: (Color white) . 
indicator backgroundColor: (Color black).
indicator contents: 'Click here'.


```



