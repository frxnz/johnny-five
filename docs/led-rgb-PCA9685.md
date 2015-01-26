# Led Rgb PCA9685

Run with:
```bash
node eg/led-rgb-PCA9685.js
```


```javascript
var five = require("johnny-five");


five.Board().on("ready", function() {

  // Initialize the RGB LED
  var led = new five.Led.RGB({
    pins: {
      red: 0,
      green: 1,
      blue: 2
    },
    controller: "PCA9685"
  });

  // RGB LED alternate constructor
  // This will normalize an array of pins in [r, g, b]
  // order to an object (like above) that's shaped like:
  // {
  //   red: r,
  //   green: g,
  //   blue: b
  // }
  // var led = new five.Led.RGB({
  //   pins: [0, 1, 2],
  //   controller: "PCA9685"
  // });

  // Add led to REPL (optional)
  this.repl.inject({
    led: led
  });

});

```


## Breadboard/Illustration


![docs/breadboard/led-rgb-PCA9685.png](breadboard/led-rgb-PCA9685.png)
[docs/breadboard/led-rgb-PCA9685.fzz](breadboard/led-rgb-PCA9685.fzz)





## License
Copyright (c) 2012, 2013, 2014 Rick Waldron <waldron.rick@gmail.com>
Licensed under the MIT license.
Copyright (c) 2014, 2015 The Johnny-Five Contributors
Licensed under the MIT license.
