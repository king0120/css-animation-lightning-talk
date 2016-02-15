#Web Animations

##CSS
When to use CSS Animations
 - Simple hover states
 - Fade-In, Fade-Out
 - Changing UI states
### How can I animate in CSS?
CSS Animations happen either through Keyframe Animations or Transition.

###Transition
Transitions allow you to control animation speed when changing CSS properties.  Normally, this change is instinaous, but by using transition you can create a smooth animation.
The following properties can be effected by Transition: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_animated_properties

Transition has 4 total properties 
- transition-property
- transition-delay
- transition-timing-function
- transition-duration

Shorthand:
transition: property name | duration | timing function| delay
transition: margin-left 4s ease-in-out 1s;

ex: 
http://codepen.io/king0120/pen/qbvPOE

###Keyframes
Keyframes are created through the animation property and keyframes. 

Keyframes are created by calling @keyframes within your css file.

@keyframes moveLeft {
	from {
		margin-left: 100%
	}
	to {
		margin-left: 0;
	}
}

Keyframes can also be directed via percentages

@keyframes moveEverywhere {
	0% {
		margin-left: 100%
	}
	10% {
		margin-left: 30%
	}
	30% {
		margin-left: 50%
	}
	50% {
		margin-left: 0%
	}
	70% {
		margin-left: 60%
	}
	100% {
		margin-left: 100%
	}
}

These keyframe animations are called through the animation property.  Animation has the following properties.

animation-delay: Delay amount in s(seconds) or  ms(milliseconds)

animation-direction: normal | reverse | alternate | alternate-reverse

animation-duration: Duration in s(seconds) or  ms(milliseconds)

animation-iteration-count: Number of times the animation should play, can be infinite or a decimal.

animation-name: The name of the keyframe definted earlier in the file.

animation-play-state: running | paused

animation-timing-function: The timing function defined by keyword (ease-in, ease-out, etc) or bezier-curve

animation-fill-mode: none | forwards | backwards | both

###What can I animate?
 ###Transform
##Javascript
When to use Javascript Animations
	- When you need to create animations with multiple parts.  
	- Advanced effects such as bouncing, pausing, rewind, slow-mo, etc.

	



##Great Examples of Web Animation
https://kamra.invisi-dir.com/
http://2016.makemepulse.com/