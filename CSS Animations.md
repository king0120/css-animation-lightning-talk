#Web Animations

##CSS
When to use CSS Animations

 + Simple hover states
 + Fade-In, Fade-Out
 + Changing UI states


### How can I animate in CSS?
CSS Animations happen either through Keyframe Animations or Transition.

####Transition
Transitions allow you to control animation speed when changing CSS properties.  Normally, this change is instinaous, but by using transition you can create a smooth animation.
The following properties can be effected by Transition: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_animated_properties

Transition has 4 total properties 

+ transition-property
+ transition-delay
+ transition-timing-function
+ transition-duration

Shorthand:

**transition**: property name | duration | timing function| delay

ex: 
http://codepen.io/king0120/pen/qbvPOE

####Keyframes
Keyframes are created through the animation property and keyframes. 

Keyframes are created by calling @keyframes within your css file.

```
@keyframes moveLeft {
	from {
		margin-left: 100%
	}
	to {
		margin-left: 0;
	}
}
```

Keyframes can also be directed via percentages

```
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
```

ex: 
http://codepen.io/king0120/pen/qbvPOE

These keyframe animations are called through the animation property.  Animation has the following properties.

 + animation-delay: Delay amount in s(seconds) or  ms(milliseconds)

 + animation-direction: normal | reverse | alternate | alternate-reverse

 + animation-duration: Duration in s(seconds) or  ms(milliseconds)

 + animation-iteration-count: Number of times the animation should play, can be infinite or a decimal.

 + animation-name: The name of the keyframe definted earlier in the file.

 + animation-play-state: running | paused

 + animation-timing-function: The timing function defined by keyword (ease-in, ease-out, etc) or bezier-curve

 + animation-fill-mode: none | forwards | backwards | both

Shorthand:

**animation**: duration | timing-function | delay | 
   iteration-count | direction | fill-mode | play-state | name

###What can I animate?
 Keyframe animations can be used by all properties that can use transitions
 
##Javascript
When to use Javascript Animations

+ When you need to create animations with multiple parts.  
+ Physics based motions
+ Advanced effects such as bouncing, pausing, rewind, slow-mo, etc.

###Animation Libraries

There are plenty of great animation libraries available today.  Today I am going to cover Velocity.js but there are other options available

jQuery:
Greensock: http://greensock.com/gsap
Velocity.js

####Velocity.js
Velocity.js is a lightweight library with a syntax that is familiar to anyone using jQuery.  In fact, you can replace $.animate with $.velocity() anywhere in your project and be perfectly fine.  

I chose to cover Velocity.js due to it's speed and it's smoothness compared to jQuery.

###$.velocity

The $.velocity method (or $.animate in jQuery) is the core of Javascript animation.

The method's first argument is the CSS properties that are going to be altered and the second is an optional object that sets Velocities options

```
$element.velocity({
    width: "500px",
    property2: value2
}, {
    /* Velocity's default options */
    duration: 400,
    easing: "swing",
    queue: "",
    begin: undefined,
    progress: undefined,
    complete: undefined,
    display: undefined,
    visibility: undefined,
    loop: false,
    delay: false,
    mobileHA: true
});
```

####Fade & Slide
Velocity has easy fade ins and slide outs through the following syntax

```
$element.velocity('fadeIn', {duration: 1000})
		.velocity('fadeOut',{delay: 500, duration: 1000})
```

####Scroll
One of the more popular features of velocity is it's easy to use scroll function.  To use scroll, set the first argument of $.velocity() to 'scroll' and the second argument sets parameters relevant to the scroll.  The following parameters can be set 

- container: Scroll to a specific id or div
- axis: Scroll across a x or y axis
- offset: Scroll

##Great Examples of Web Animation
https://kamra.invisi-dir.com/

http://2016.makemepulse.com/