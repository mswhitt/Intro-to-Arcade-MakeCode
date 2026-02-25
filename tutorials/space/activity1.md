# Asteroid Blaster


## Introduction @unplugged

** Let's explore the depths of space! **

In this tutorial, you'll create your own asteroid destroying masterpiece.

![Flying through space](/static/skillmap/space/asteroid-blaster.gif "Blasting through a starfield" )

## Set the scene
**Give 'em something to look at** 🔭

---


🔲 Drag the ``||scene:start screen [confetti] effect ⊕||`` from the  ``||scene:Scene||`` category and
into the ``||loops:on start||`` block that's already in the workspace.

🔲 Next, select ``||scene:star field||`` (instead of ``||scene:confetti||``) from the dropdown
and watch as you blast into space! 🚀 


---


```blocks
// @highlight
effects.starField.startScreenEffect()
```



## Draw your ship
**🧑🏿‍🚀 Time to choose our ship! 👩🏾‍🚀**

---

🔲 From the ``||sprites:Sprites||`` category, drag the ``||variables:set [mySprite] to sprite [ ] of kind [Player]||`` 
block  and place it at the end of the ``||loops:on start||`` container.

🔲 Click on the grey box in the middle of your
 ``||variables:set [mySprite] to sprite [ ] of kind [Player]||`` block
to design a ship of your own! Are you a rusty pile of scraps or a sleek, futuristic rocket?

---

**Tip:** Don't feel like drawing your ship? Once you're in the sprite editor,
flip to the gallery and choose from premade images.

```blocks
effects.starField.startScreenEffect()
// @highlight
let myShip = sprites.create(img`
    .....................
    .....................
    .........666.........
    ........26c62........
    .......26c1c62.......
    ......26c1d1c62......
    .....2661ddd1662.....
    ....2661ddddd1662....
    ...666cdddddddc666...
    ..666616ddcdd616666..
    ..6666d.1dcd1.d6666..
    .6666..1d...d1..6666.
    .6666.1d.....d1.6666.
    .666..d.......d..666.
    .6666.d1.....1d.6666.
    .666dddd1...1dddd666.
    .666dc..ddddd..cd.66.
    .66..66.......66..66.
    .66...6.......6...66.
    ..66.............66..
    .....................
    `, SpriteKind.Player)
```

## Control your ship

🌟 Let's get your ship moving 🌟

---

🔲 Find the ``||controller:move [mySprite] with buttons ⊕||`` block 
and drag it into the bottom of the ``||loops:on start||`` container. 

🔲 Set both vx and vy to 50


```blocks
effects.starField.startScreenEffect()
let myShip = sprites.create(img`
    .....................
    .....................
    .........666.........
    ........26c62........
    .......26c1c62.......
    ......26c1d1c62......
    .....2661ddd1662.....
    ....2661ddddd1662....
    ...666cdddddddc666...
    ..666616ddcdd616666..
    ..6666d.1dcd1.d6666..
    .6666..1d...d1..6666.
    .6666.1d.....d1.6666.
    .666..d.......d..666.
    .6666.d1.....1d.6666.
    .666dddd1...1dddd666.
    .666dc..ddddd..cd.66.
    .66..66.......66..66.
    .66...6.......6...66.
    ..66.............66..
    .....................
    `, SpriteKind.Player)
controller.moveSprite(myShip, 50, 50)
```

## Stay in screen

**Uh-oh, if you move off screen, your ship disappears!**

---

🔲 To keep your ship from exploring beyond the edges, find
 the ``||sprites:set [mySprite] stay in screen <on>||`` block and
snap it in at the end of the program.
 


```blocks
effects.starField.startScreenEffect()
let myShip = sprites.create(img`
    .....................
    .....................
    .........666.........
    ........26c62........
    .......26c1c62.......
    ......26c1d1c62......
    .....2661ddd1662.....
    ....2661ddddd1662....
    ...666cdddddddc666...
    ..666616ddcdd616666..
    ..6666d.1dcd1.d6666..
    .6666..1d...d1..6666.
    .6666.1d.....d1.6666.
    .666..d.......d..666.
    .6666.d1.....1d.6666.
    .666dddd1...1dddd666.
    .666dc..ddddd..cd.66.
    .66..66.......66..66.
    .66...6.......6...66.
    ..66.............66..
    .....................
    `, SpriteKind.Player)
controller.moveSprite(myShip, 50, 50)
// @highlight
myShip.setStayInScreen(true)

```

## Setup life and score

**Uh-oh, if you move off screen, your ship disappears!**

---

🔲 Use ``||info:set life to 3||`` to start the player off with some life

🔲 Use ``||info:set  score to 0||`` to start the player off with no score


```blocks
effects.starField.startScreenEffect()
let myShip = sprites.create(img`
    .....................
    .....................
    .........666.........
    ........26c62........
    .......26c1c62.......
    ......26c1d1c62......
    .....2661ddd1662.....
    ....2661ddddd1662....
    ...666cdddddddc666...
    ..666616ddcdd616666..
    ..6666d.1dcd1.d6666..
    .6666..1d...d1..6666.
    .6666.1d.....d1.6666.
    .666..d.......d..666.
    .6666.d1.....1d.6666.
    .666dddd1...1dddd666.
    .666dc..ddddd..cd.66.
    .66..66.......66..66.
    .66...6.......6...66.
    ..66.............66..
    .....................
    `, SpriteKind.Player)
controller.moveSprite(myShip, 50, 50)
myShip.setStayInScreen(true)
// @highlight
info.setLife(3)
// @highlight
info.setScore(0)
```

