# Scripts

In Tableaunoir, you can use scripts to boost your creativity! You can write any Javascript code + function from [https://github.com/tableaunoir/tableaunoir/blob/master/src/Script.ts]. But let us discuss some examples.


## Tableaunoir sings!

This example illustrates how to add music when drawing. See [https://www.youtube.com/watch?v=IXy4FrHXFCo].

```javascript
let o = S.newOscillator()
let b = false;

S.onupdate = () => {
    if (ismousedown) {
        if (!b) {
            o = S.newOscillator()
            o.start();
            b = true;
        }
        S.setFrequency(o, musicScoreYToFrequency(point.y));
    }
    else {
        if (b) {
            o.stop()
            b = false;
        }
    }
}
```

## Seesaw

This example illustrates how to move magnets automatically to have an animation.

![Seesaw](img/seesaw.gif)

```javascript
A.addEventListener("pointermove", 
     () => {S.magnetMove(B, S.center(B).x, 1000-S.center(A).y);
            S.magnetMove(A, 300, S.center(A).y); })
```

## Scratching

You may scratch a zone and discover the set of points in the plane that satisfy some conditions. In the example, a convex polygon (in green).

![Scratching](img/scratching.gif)

```javascript
  S.onmousemove = ({ x, y }) => {
      x = S.round1(7 * (x - 239) / (880 - 239));
      y = S.round1(-7 * (y - 820) / (820 - 239));
      const a = S.round1(5 * x - 2 * y);
      const b = S.round1(7 - x - y);
      const c = S.round1(5 - x);
      S.magnetSetText(m112801, `x=${x} </br> y=${y}   </br> a=${a}  </br>   b=${b}   </br>  c=${c}`);
      S.setColor((a >= 0 && b >= 0 && c >= 0 && x >= 0 && y >= 0) ? "#008822" : "#220000");
 }
```
     
     
    
## Car game

Make a car game in Tableaunoir in 30sec. Draw a map, draw a car, transform the car in magnet and load the script below!

![cargame](img/cargame.gif)

```javascript
let angle = 0;
let speed = 0;
let c = {x: 200, y: 200};
let car = S.getMagnets()[0];

function control() {
    if(keys["a"]) angle-=0.05;
    if(keys["e"]) angle+=0.05;
    if(keys["z"]) speed += 0.5;
    speed = Math.min(10.0, speed);
    car.style.transform = `rotate(${angle}rad)`;
};

S.onupdate = () => {
    control();
    speed -= 0.2;
    speed = Math.max(0.0, speed);
    const nc = {x: c.x, y: c.y};
    nc.x += speed * Math.cos(angle);
    nc.y += speed * Math.sin(angle);
    nc.x = Math.max(0.0, nc.x);
    nc.y = Math.max(0.0, nc.y);
    nc.x = Math.min(2000.0, nc.x);
    nc.y = Math.min(1000.0, nc.y);

    if(!S.magnetDrawingUnder(car, nc.x, nc.y))
        c = nc;
    S.magnetMove(car, c.x, c.y);
}
```

## More scripts?

You can open a pull-request and suggest one of your script!
