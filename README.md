# svg-animation
SVG Animation Presentation
https://iralitv.github.io/svg-animation/#/

Youtube video:


## Script
* #### 0 slide (SVG)
SVG is an image format that is based on XML, much like how HTML works. It defines different elements for a number of familiar geometric shapes that can be combined in the markup to produce two-dimensional graphics.
But wait, we should start from begin, precisely speaking from reasons of creating.

* #### 1 slide (typically frontend relationship with image animation)
**1.1** Any front-end engineer worth their salt is aware of the challenges that the fragmented ecosystem of devices brings.

**1.2** Can you even zoom usual image? What did you see? Right. It’s pixalated. And it’s size around hudreds of kylobytes. And developers had to dodge constantly so that the pictures looked acceptable.

**1.3** Different screen sizes, resolutions, and aspect ratios make it difficult to deliver a consistent experience. More so for those who want to deliver a pixel-perfect experience.
And solution is exist! SVG!

* #### 2 slide (SVG? WTF?)
**2.1** Scalable Vector Graphics help in solving a part of that problem, and do it very well. 
Although they have their limitations, SVGs can be very helpful for certain occasions and, if you have a good design team, you can also create a more visually stunning experience without putting undue burden the web browser or hampering the load times.

**2.2** WHY SVG ANIMATION?
*	Lightweight
*	Fast
*	Scalable
*	Lots of online tutorials
*	Interactivity
*	Supported on all major browsers (except IE8 and less)
* ####3 slide
**3.1** SVG Paths
If there is one overpowered element in SVG, that would be the <path> element.
The path element is a basic shape that may be used to create almost any advanced 2D shape you can imagine.
The element works by taking a sequence of drawing commands. It is a lot like the Logo programming language from 1967, only modernized and designed for fancy graphics. 

**3.2** The element takes this sequence of drawing commands through the attribute d.
`<path d="M10 10 L75 10 L75 75 Z" />`
You can think of a virtual pen that draws on the screen, and the drawing comments in the path element merely controls the pen. In the example above, the pen is being instructed to move to position (10, 10) (M10 10), to draw a line to (75, 10) (L75 10), to draw a line to (75, 75) L75 75 and then to close the path by returning to the starting point (Z).

**3.3** Using other drawing commands, such as arcs (A), quadratic bezier curves (Q), cubic bezier curves (C), etc you can create much more complex shapes and graphics in SVG.

* #### 4 slide
**4.1** “Okay Ira, I get it. Paths are powerful, but how do I animate them?” you say.

**4.2** SVG animation can be 3 types. First with help CSS, the second one is native animation, and the last it’s adding interactivity with JS libraries.

* #### 5 slide
**5.1** CSS keyframes is most popular type of item animation. 

**5.2** For our first technique, we are going to take advantage of two SVG attributes: stroke-dasharray and stroke-dashoffset.
The stroke-dasharray attribute controls the pattern of dashes and gaps used to stroke the path. If you wanted to draw your lines as a group of dashes and gaps instead of one continuous stroke of ink, this is the attribute you would use.
With SVG images being a part of the web browser’s DOM and stroke-dasharray being a presentation element, the attribute can also be set using CSS.

**5.3**  Similarly, the stroke-dashoffset attribute (which specifies how far into the dash pattern to start the dash) can also be controlled using CSS.
These two SVG attributes, together, can be used to animate SVG paths, giving the viewer the illusion that the paths are being drawn gradually.
Take this quadratic bezier curve, for example:

`<path fill="transparent" stroke="#000000" stroke-width="5" d="M10 80 Q 77.5 10, 145 80 T 280 80" class="path"></path>` 

As you can see, the curve is always there. 

**5.4** We are only changing the dash offset to make the dashed part appear bit by bit.

**5.5** You can take this a step further by using the same principle but with more paths.

**5.6** And we add more styles, after that add more animations

**5.7** Here you have one black curve that is fixed, a red one that is moving along the path, and another black one following the red one but 40px behind.
Stroke-dasharray and stroke-dashoffset are two very powerful attributes that can be used to apply a plethora of animations and effects to your SVG paths. You can try this tool that you can use to experiment with the two attributes.

* #### 6 slide Native animation
**6.1** Animation is done by manipulating the attributes of shapes over time. This is done using one or more of the 4 SVG animation elements.

**6.2** ELEMENTS. 
Animation is achieved by nesting one or more of the following elements inside the element that needs animation.
•	Set
•	Animate
•	animateMotion
•	animateTransform

**6.3** The `<animate>` tag is nested with the open tag of the object to be animated. It does not work for paths, consists of coordinates, but only inside tags, creates objects.

**6.4** animateMotion is allowing you to move an element along a given path. You can see the rectangle moves on path of curve line.

**6.5 animationTransform rotate** 
This type of transformation rotates the figure around, according to the indicated degrees. Rotation works relative to the value of degrees, the most rotating figure.

**6.6 animationTransform scale** 
This kind of transformation increases the size according to the X axis (width) and according to the Y axis (height).
Scale values increase the original shape size. For example, if we set the value of scale X to 3, the figure will become three times wider. If you set the scale Y value to 3, the figure will become three times higher, it will look like this:
Note the additive attribute. It shows that animations do not override each other, but instead work in the same time.

**6.7 Combine animation** 
Synchronize beginning of one animation to end of another. Also we can add interactivity by click with attribute begin. In the second animation this attribute has value first.end. It means the second animation start after ending the first one.

* #### 7 slide JS animation
**7.1** For SVG animation we don’t use vanilla JS. SVG become very popular in frontend industry. And it’s main reason why we have so many libraries for animate SVG.

**7.2** the most popular are: Snap.svg, GSAP, Velocity.js, Svg.js, Raphael.js

**7.3** And I want to show you the cool animation obtained using GSAP library.

**7.4** GSAP is paid library. But for CodePen it’s free. So you can play with animation there. So we can get from this picture something like this. 

**7.5** You can see this wonderful snow and the day is changed by night and it's repeat.
* #### 8 slide 
It’s all for today. Thanks.

