# Political-fifth
It's a candy

![buh](https://github.com/nicolasbaez/Political-fifth/blob/main/xp017.gif)
```javascript
setup = (_) => createCanvas((w = 500), w, WEBGL);
draw = (_) => {
  colorMode(HSB, 3);
  clear();
  rotateX(w);
  rotateY(w / 2);
  r = 99;
  noFill();
  for (i = 0; i < 3; i += map(sin(w), 0, 1, 1, 0.1)) {
    beginShape();
    for (j = 0; j < 7; j += 0.1) {
      stroke(i, j, 3);
      vertex(r * sin(i) * cos(j), r * sin(i) * sin(j), r * cos(i));
    }
    endShape();
  }
  w -= 0.01;
};
keyPressed = (_) => {
  if (key === "s") {
    saveGif("xp017.gif", 1005, { delay: 0, units: "frames" });
  }
};
