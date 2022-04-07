# Make a presentation / animation

With Tableaunoir, you can create **animated courses / presentations**. You can then:
- make **presentations** that is a document made up with consecutive **slides** (by pressing PageDown and PageUp you will move in your slides)
- make **animated GIFs** (together with the software [Peek](https://github.com/phw/peek) for instance)
- make **videos** (together with the software OBS)


## Example of an animated proof

Here is an example of a GIF made with Tableaunoir. This little GIF explains why the square root of 2 is [irrational](https://en.wikipedia.org/wiki/Irrational_number).

![proofsqrt2irrational](img/proofsqrt2irrational.gif)

Please also find an example of video: [https://www.youtube.com/watch?v=SsBujkaOnr4]

## Animation mode!

Tableaunoir stores your course but also its **evolution in time**. If you want all the states of your blackboard, click on the animation/replay button in the toolbar:

![buttonReplay](img/buttonReplay.png)





## Navigation in your course

The timeline is displayed a the bottom of the screen. The progress bar is similar to the one of a Youtube video: the past is represented in red; while the future is in grey.

![screenshot_animation](https://user-images.githubusercontent.com/43071857/162198738-dc62f403-77c2-4fb0-a9d7-927ae1f6c58d.png)

There are three buttons. The left and right arrows are for navigating in the presentation (last and next slides). The third button (hearts) proposes a menu to add new slides and to merge slides. Below the progress bar, each little square represents an atomic action. An atomic action can be: a drawing, erasing something, erasing the full board, adding a magnet, deleting a magnet, moving a magnet, etc. When you click on, you will reach the state of the board after that action. The first empty square (on the left) is the beginning of the slide.

## How to create animations?

Animations are easy to do with Tableaunoir, since you simply perform them. Just draw, erase, add a magnet, move a magnet, remove a magnet. Every action is automatically recorded as an animation.

In order to record from a give point in time, click on the timeline progress bar or on some action squares. Your actions will then be recorded from that point in time.



## How to add new slides?

For adding new slides, you click on the heart menu. From there, you can either create an **empty slide**. You can also create a new slide that automatically contains what was already drawn  (equivalent of `\pause` in LaTEX beamer). Another way, is to clear the board: go in the tool menu (pressing "t") and choose "Clear the board" (the icon is an eraser with a cape). Erasing the board corresponds to creating an empty slide.

## For running your animation

Press Page Down and Page Up to see your course/animation. You can also click directly in the progress bar.


## How to edit the timeline?

- Delete an action. Drag and drop a square on the top to remove that action from the list.
- Change the order of actions. Drag and drop a square in another place to change the order.
- To perform deletion/change the order of actions and slides, use Ctrl for selecting several actions and/or slides, and Shift for consecutive selections.
- You can also merge two slides, that the current and the next slides are replaced by a single one, containing the actions of the two previous slides.
