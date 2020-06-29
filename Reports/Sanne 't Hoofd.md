# UX design and CSS
#### A Lecture by Sanne 't Hoofd - February 19th

## About Sanne 't Hoofd
Sanne 't Hoofd is lecturer at the Amsterdam University of Applied Sciences. During this lecture, he showed us some examples of beautiful CSS creations by some of his students as well as some of his own work. The goal of this lecture was to inspire us to be more creative in our own work and make us aware of what can be achieved using just some CSS.

## Micro Interactions
't Hoofd gave us three characteristics that together define micro interactions.
1. A signature moment in a digital product (site, app, ...)
2. A Product based around one micro-interaction
3. People see interaction with a digital product as a series of micro interactions.

Each micro interaction can be broken down into four components using the model below:

![Micro interaction model](https://github.com/lennartdeknikker/weekly-nerd-1920/blob/master/assets/images/sanne%20t%20hoofd/micro%20interaction%20model.png)

This model was coined by *Dan Saffer* in his book *"Micro Interactions - Designing with Details."* Below each interaction component is explained in more detail:

> ### Triggers
> initiate a microinteraction. Triggers can be user-initiated and system initiated. In a > >  user-initiated trigger the user has to initiate an action, say in the medium’s clap icon. In system initiated trigger, the software detects certain rules are being met and initiates an action, say the locking of phone when it is idle for sometime.
> ### Rules
> determine what happens once a microinteraction is triggered. In the medium’s clap icon it initiates a little burst or explosion.
> ### Feedback
> lets people know what’s happening. Anything a user sees, hears, or feels while microinteraction is happening is feedback. It means that your action has been acknowledged. Remember the vibration on your phone when it is silenced or when it is switched on/off.
> ### Loops and modes
> determine the meta-rules of the microinteraction. What happens to microinteraction when conditions change or when they expire? Will the feedback be repeated?

*source: https://uxplanet.org/ux-of-microinteractions-for-user-delight-fac1baed527a*


## Playing around with CSS
't Hoofd then started off showing us some examples of [these works by his students](https://www.sinds1971.nl/spelenmetcss/index.html). These examples had no other function than to spark some user delight. It was inspiring to see how a few relatively simple micro interactions can trigger a smile on the users faces.

## The Carousel
As last example he showed us how he built [a 3D carousel](https://codepen.io/shooft/pen/zYGppvK). 

As a project for Ben & Jerry's he built [this carousel](https://www.sinds1971.nl/bj2/index.html) to show different ice cream flavours and have users browse through those in a way that makes it fun to do so. This is optimized by adding some micro interactions, like the way the carousel bounces back a little every time you give it a swing.

![ben & jerry carousel](https://github.com/lennartdeknikker/weekly-nerd-1920/blob/master/assets/images/sanne%20t%20hoofd/ben%20%26%20jerry's.png)


He showed us how he started on this project, the sketches he made and what math he used to calculate the positions and size of all the carousel items. What impressed me most was that it was possible to add a huge amount of items to the carousel without slowing it down. It did get slower when we tried to find out how far we could stretch the amount, but it seemed to be a lot lighter than when you would try the same using just javaScript.

## Conclusions
- Details are important and it's our responsibility to provide those.
- It's important to understand the users needs.
- Aim for User Delight
- It's important to experiment.
  - It's no problem to fail sometimes as long as you learn from those experiments.