# Cylon.js on Edison
examples using edison + cylon.js

### Connect wifi to the edison

connect the two usb ports

    configure_edison --wifi

  configure the wifi (for a battery powered edison I suggest making an hotspot with your phone, otherwise set it up on your router's wifi) 

Choose a stable/definitive connection you need to be connected to the edison via the digital (non-power) programming port to reconfigure the wifi.

### Install dependencies

    $ npm install cylon cylon-firmata cylon-gpio cylon-i2c

    
### Use Cylonjs
  
  with a Servo
  
    http://cylonjs.com/documentation/drivers/servo/#how-to-use

 
  how to use cylon on edison

    http://cylonjs.com/documentation/platforms/edison/#how-to-use

  also see the latest link (before python section start)
  

#### links & related projects notes: 

> #### bitswitch

### https://gist.github.com/makevoid/c9c98578040baef4375f#file-bitswitch_relay_intel_edison_nodejs-js-L38

Complete sketch (blockchain/bitcoin) oriented, has to be merged to Cylon.js code or import an arduino Servo library ( https://www.arduino.cc/en/Reference/Servo )

Well done basic idea/guide is already the there:

look at:

### http://www.codefoster.com/edison-coding/

servo code like:

```js
var Cylon = require('cylon');

var action = Cylon.robot({
  connections: {
    arduino: { adaptor: 'firmata', port: '/dev/ttyACM0' }
  },

  devices: {
    servo: { driver: 'servo', pin: 3 }
  },

  work: function(my) {
    var angle = 45 
    
    my.servo.angle(0)       // set the servo to rotation degrees 0 (starting position)
    setTimeout(function(){
        my.servo.angle(45)  // set the servo to 45* rotation
    }, 2000)
    setTimeout(function(){
        relayPin.write(0)   // set the servo to 0* rotation again
    }, 6000)
  }
});

// use this where you usually do pin.write(1), digitalWrite(x) etc..., this will trigger the work() function once
action.start()
```


---

### J5

Also look at J5 - Jhonny 5: http://johnny-five.io/#edison - Servo supported

awesome docs

http://johnny-five.io/api/servo/

http://johnny-five.io/examples/servo/



---

alternative 

#### use python:

    https://zorg-framework.github.io
