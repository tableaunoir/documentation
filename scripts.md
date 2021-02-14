# Scripts

In Tableaunoir, you can use scripts to boost your creativity! Please find some examples.

## Seesaw

This example illustrates how to move magnets automatically to have an animation.

![Seesaw](seesaw.gif)

`A.addEventListener("pointermove", () => {S.magnetMove(B, S.center(B).x, 1000-S.center(A).y); S.magnetMove(A, 300, S.center(A).y); })`
