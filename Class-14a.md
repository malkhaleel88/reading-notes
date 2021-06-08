# **CSS Transforms, Transitions, and Animations**

## **CSS Transforms**

*The transform property applies a 2D or 3D transformation to an element. This property allows you to rotate, scale, move, skew, etc., elements.*

*The actual syntax for the transform property is quite simple, including the transform property followed by the value. The value specifies the transform type followed by a specific amount inside parentheses.*

**With the CSS `transform` property you can use the following 2D transformation methods:**
```
* translate()
* rotate()
* scaleX()
* scaleY()
* scale()
* skewX()
* skewY()
* skew()
* matrix()
```

**3D transforms use the same transform property used for 2D transforms. If you’re familiar with 2D transforms, you’ll find the basic 3D transform functions similar.**
```
rotateX( angle )
rotateY( angle )
rotateZ( angle )
translateZ( tz )
scaleZ( sz )
```

## **CSS Transitions and Animations**

### **CSS Transitions**

*CSS transitions allows you to change property values smoothly, over a given duration.

#### **CSS Transition Properties**

* **transition** - *A shorthand property for setting the four transition properties into a single property.*

* **transition-delay** - *Specifies a delay (in seconds) for the transition effect.*
* **transition-duration** - *Specifies how many seconds or milliseconds a transition effect takes to complete.*
* **transition-property** - *Specifies the name of the CSS property the transition effect is for.*

* **transition-timing-function** - *Specifies the speed curve of the transition effect.*

### **CSS Animation**

*An animation lets an element gradually change from one style to another.*

*You can change as many CSS properties you want, as many times as you want.*

*To use CSS animation, you must first specify some keyframes for the animation.*

*Keyframes hold what styles the element will have at certain times.*

#### **CSS Animation Properties**

* **@keyframes** - *Specifies the animation code.*
* **animation** - *A shorthand property for setting all the animation properties.*
* **animation-delay** - *Specifies a delay for the start of an animation.*
* **animation-direction** - *Specifies whether an animation should be played forwards, backwards or in alternate cycles.*
* **animation-duration** - *Specifies how long time an animation should take to complete one cycle.*
* **animation-fill-mode** - *Specifies a style for the element when the animation is not playing (before it starts, after it ends, or both).*
* **animation-iteration-count** - *Specifies the number of times an animation should be played.*
* **animation-name** - *Specifies the name of the @keyframes animation.*
* **animation-play-state** - *Specifies whether the animation is running or paused.*
* **animation-timing-function** - *Specifies the speed curve of the animation.*


[HOME](https://malkhaleel88.github.io/reading-notes)