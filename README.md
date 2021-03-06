####iOS-Flip-Transform

####Summary:  
Animation component for the effect of flipping as in a news/clock ticker, or a page turn. 

Structured around the idea of a data object (i.e. headline in news, number in a clock, page in a book) as an animation frame, comprised of multiple CALayers.

Supports 3 interaction modes:  
Triggered - as in a tap to flip  
Auto - as in a revolving flip that loops through data  
Controlled - as in a pan gesture that moves the flip layer according to touch

Supports different types of content:  
Blank, with background color  
With image (whether from file or screenshot)  
With dynamic text, either composited on background or on image

Supports customizable parameters:  
Sensitivity, gravity, shadow, text positioning, alignment, font etc.

####Basic Usage:

1. Create delegate object -  
AnimationDelegate *animationDelegate = [[AnimationDelegate alloc] initWithSequenceType: directionType:];

2. Create flip view and assign it to animation delegate -   
FlipView *flipView = [[FlipView alloc] initWithAnimationType: animationDelegate: frame:];  
animationDelegate.transformView = flipView;

3. Add flip view as subview and customize properties

4. Call [flipView printText: usingImage: backgroundColor: textColor:] to draw each frame (minimum of 2)

5. Call [animationDelegate startAnimation:] to start the animation. For using buttons or pan gesture, look at the animation controller example
