# PharoByExample150

By the book , captain - spock - the wrath of khan - star trek.

Lets get started .

This is a very simple introduction to Pharo smalltalk , what you learn here is applicable to every Smalltalk.

To install pharo - you can download and run the launcher 

![The launcher](docs/Chapters/Chapter1/figures/pharo-launcher-2026-05-23_20-07.png)

click new for a new image

![The launcher](docs/Chapters/Chapter1/figures/launcher-click-the-new-image-button-2026-05-23_23-12.png)

now click create image

![The launcher](docs/Chapters/Chapter1/figures/launcher-click-create-image-button-2026-05-23_23-08.png)

select desired version of Pharo required 

![The launcher](docs/Chapters/Chapter1/figures/launcher-select-desired-version-2026-05-23_23-20.png)

finally click Launch to start using Pharo 

![The launcher](docs/Chapters/Chapter1/figures/launcher-click-launch-button-2026-05-23_23-21.png)


# Pharo first steps 

you should be greeted with a window that looks something like this

![Start of Pharo](docs/Chapters/Chapter1/figures/pharo-welcome-14-2026-05-23_20-11.png)

This is the welcome screen of Pharo 

As a beginner you will want to start with the Playground.

You can open a playground by pressing Ctrl + O + P .

Holding down the 'Control key' - your keyboard may have a key that says 'Ctrl' . 

While keeping the 'Control key' pressed down , press and *release* the letter 'O' key - O for Oranges , now press and *release* the letter 'P' key - P for Peter .

you should hopefully see something like this , it will say Playground on the title of the window

![Empty Playground](docs/Chapters/Chapter1/figures/empty-playground-2026-05-23_22-49.png)

In Smalltalk something surrounded by single quotes is interpreted as a String.

![Single quote character](docs/Chapters/Chapter1/figures/single-quote.jpg)

Lets type a quick program into the playground

```
'Hello' reverse. 
```

![Playground](docs/Chapters/Chapter1/figures/playground-step1-2026-05-23_20-32.png)

Lets run this program 

![Playground](docs/Chapters/Chapter1/figures/click-the-do-it-all-button-2026-05-23_23-48.png)

Alternatively we can select code and right click 'Do it and go' .  This will mean the results go into next movie slide to the right of current code window.

![Playground](docs/Chapters/Chapter1/figures/action-consequence-2026-05-24_02-47.png)

This box that has opened up to the right is called an Inspector.  The inspector allows us special access inside the result that we got handed back. In this case the letters of Hello reversed or rather olleH .

![Inspector](docs/Chapters/Chapter1/figures/the-inspector-bubble-2026-05-24_02-39.png)

Lets return to this result from reversing the string 'Hello' .

![Inspector](docs/Chapters/Chapter1/figures/plain-result-reversed-2026-05-23_23-45.png)

We can see the result is a ByteString. 

![Inspector](docs/Chapters/Chapter1/figures/inspector-result-is-a-bytestring-2026-05-23_23-43.png)

The result is displayed in what is called the Inspector. The inspector is capable of making different views of a result. The preview tab is currently selected , preview can be likened to a quick glimpse of an object.

![Inspector](docs/Chapters/Chapter1/figures/different-views-inspector-2026-05-24_03-19.png)

The items view tab shows letters of the string in a numbered list format , so can see for instance the fourth letter of the string 'olleH' is the letter `$e` . A dollar sign infront of a letter in Smalltalk means that it is taken to mean a character.

![Inspector](docs/Chapters/Chapter1/figures/string-items-2026-05-24_03-24.png)

The full content tab shows all of the string

![Inspector](docs/Chapters/Chapter1/figures/full-content-string-2026-05-24_03-27.png)

There are a few other tabs but last is common to all objects and is called the meta tab. The meta tab shows the class hierarchy , methods and one method selected shows its own source code.

We see for the first time the true horror of inheritance ByteString inherits from String . String inherits from ArrayedCollection.  ArrayedCollection inherits from SequenceCollection , and on and on and on.

![Inspector](docs/Chapters/Chapter1/figures/meta-class-tab-inspector-2026-05-24_03-31.png)

### Human genomic strings

To understand the true scale of computing today the human genome string is reported to be 3.2 billion base pairs.  Understanding how to work with such a large 'string' takes a different approach that to say a string is an array which can be allocated on the heap and job done.

```
The haploid human genome consists of approximately 3.2 billion base
pairs (specifically 3,286,906,305 bp).  This genetic string requires
about 750 megabytes of digital storage space to represent.

Physical Length: If stretched out, the DNA in a single diploid cell
(containing two copies of the genome) is approximately 206 centimeters
(about 6.7 feet) long.  Total Body Length: The total length of nuclear
DNA in a single human individual, across all nucleated cells, extends
roughly 6.2 billion kilometers, which is enough to travel to the Sun
and back more than 41 times.  Composition: The genome is divided into
24 distinct nuclear chromosomes (22 autosomes plus X and Y) and a much
smaller mitochondrial genome of 16,569 base pairs.
```

What type of questions are asked of a genomic string ? 

What are base pairs ? 

What are these A C G and T things ? 

what is DNA ? 

how does it differ from RNA of plants ?

how does a potato self replicate ?


# Track 

We can ask how many letters are in the string 'olleH' . 


Write this into the ByteString (olleH) inspector code area , select the code - then press Control g.

```
self size
```

![Inspector](docs/Chapters/Chapter1/figures/self-size-inspector-2026-05-24_03-58.png)

Not surprisingly the result is 5 

![Inspector](docs/Chapters/Chapter1/figures/the-result-is-five-2026-05-24_03-59.png)

Now close the last inspector

![Inspector](docs/Chapters/Chapter1/figures/now-close-this-inspetor-2026-05-24_04-01.png)

Write this into the ByteString (olleH) inspector code area , select the code - then press Control g.

```
'olleH' size.
```

![Inspector](docs/Chapters/Chapter1/figures/hello-reversed-do-it-and-go-2026-05-24_04-02.png)

We can see the result again is 5 .

![Inspector](docs/Chapters/Chapter1/figures/again-the-result-is-five-2026-05-24_04-03.png)

# OK OK OK 


Selecting code and pressing Control g runs 'Do it and Go' procedure.  This will evaluate the code and if happy open an inspector window on the result.  We could also have written 


![Inspector](docs/Chapters/Chapter1/figures/self-is-olleH-2026-05-24_03-05.png)



Again the result is 5 .



We note that we can compute anything in either window we wish . 

![Inspector](docs/Chapters/Chapter1/figures/we-can-compute-anything-here-2026-05-24_01-26.png)




![Inspector](docs/Chapters/Chapter1/figures/click-this-to-close-last-inspector-2026-05-24_02-33.png)



![Inspector](docs/Chapters/Chapter1/figures/five-greater-than-four-is-true-2026-05-24_01-09.png)

finding the answer is indeed five as expected 

![Inspector](docs/Chapters/Chapter1/figures/result-small-integer-five-2026-05-23_23-59.png)

what is nice is the ability to drill down as deep as want.

Lets check our sanity that five really is greater than four.  In Pharo this looks like 

```
5 > 4 
```

![Inspector](docs/Chapters/Chapter1/figures/sanity-check-five-is-greater-than-four-2026-05-24_02-10.png)

We select the code ``` 5 > 4 ``` then right click mouse and choose 'Do it and Go' . Another inspection window will open like the next frame of a movie to the right , showing the result of the computation.

![Inspector](docs/Chapters/Chapter1/figures/check-five-is-greater-than-four-2026-05-24_02-12.png)

Thankfully it is still correct.

# Delay introduction of concept of self 


We are saying given the result i have just received - namely the SmallInteger (5) , is it greater than `>` , 4 

```
self > 4 
```

![Inspector](docs/Chapters/Chapter1/figures/self-is-the-number-five-2026-05-24_01-08.png)

We can now say for definite that five really is greater than four

![Inspector](docs/Chapters/Chapter1/figures/five-greater-than-four-is-true-2026-05-24_01-09.png)

It is important to note that the word self has special meaning in smalltalk.

Let us look once again at the size of a ByteString . We can drill down by selecting what we 
want to examine further by selecting the code and typing Control g .

This will tell pharo to 'Do it and Go' .

![Inspector](docs/Chapters/Chapter1/figures/self-size-do-it-and-go-2026-05-24_01-31.png)

Now we see two inspection windows which both refer to their own self . 

The self on the left bubble is talking about a ByteString . 

The self on the right bubble is talking about the SmallInteger (5) .

![Inspector](docs/Chapters/Chapter1/figures/different-self-bubbles-2026-05-24_01-42.png)







# recap 


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


ellipse := EllipseMorph new openInWorld ; color: (Color white alpha: 0.0) ; borderWidth: 5 ; borderColor: (Color orange) ; extent: 300@300 ; yourself.



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

really annoying to have to keep trying to find the edge of the playground

lets create a button which will send the playground to the back of the stack

Lets create a playground class with slots '#play' and '#button'.
```
Object << #GoodPlayground
	slots: { #play . #button };
	package: 'YourTools'
```

```
initialize

 "lets create a simple playground with some initial content"
	play := StPlayground openContents: self playgroundContents. 

	"lets create a simple button to do something useful "
	button := SimpleButtonMorph new
		          label: 'Run Code';
		          target: self;
		          actionSelector: #processInput:;
		          arguments: { play };
		          color: Color black;
		          yourself. 
	"Add button to world or another morph"
	button openInWorld.
```

something for the playground to initially show when it opens up 

```
playgroundContents 
^ '''Hello'' reverse.'
```

and the all important function we needed at start to send the thing to the back , 


```
processInput: aSpWindowPresenter
aSpWindowPresenter window sendToBack.
```

so my hand morphs and circles etc can be drawn over top of the playground

we can change text on the SimpleButtonMorph

```
self label: 'Send to Back'.
```


