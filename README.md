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
    
    

#### links & related projects notes: 

> #### bitswitch

### https://gist.github.com/makevoid/c9c98578040baef4375f#file-bitswitch_relay_intel_edison_nodejs-js-L38

Complete sketch (blockchain/bitcoin) oriented, has to be merged to Cylon.js code or import an arduino Servo library ( https://www.arduino.cc/en/Reference/Servo )



---

alternative 

#### use python:

    https://zorg-framework.github.io
