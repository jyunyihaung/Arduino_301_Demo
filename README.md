# Arduino_301_Demo
CiA301 on Arduino
=======
# CANOpenNode

## CH0 Create a new ino project

## CH1 Add CANOpenNode stack as submodule

```
$ git submodule add https://github.com/CANopenNode/CANopenNode.git
$ git submodule init
$ git submodule update
```

## CH11 Add header into ino project

Add CANOpenNode header into ino project, add following code to header of code:

``` c++
#include "CANopenNode\CANopen.h"
```

The code of ino project should be looks like this:

```c++
#include "CANopenNode\CANopen.h"

void setup() {
  // put your setup code here, to run once:

}

void loop() {
  // put your main code here, to run repeatedly:

}
```

## CH12 First Build ino project and get fail

Done of the operation of CH11, start build will get error message looks like this:

```
Arduino\CANOpenNode\CANopenNode\301\CO_driver.h:32:10: fatal error: CO_driver_target.h: No such file or directory
 #include "CO_driver_target.h"
          ^~~~~~~~~~~~~~~~~~~~
compilation terminated.
exit status 1
Error compiling for board Arduino Uno.
```

This message shows there is a missing file, take a look into README.MD of CANOpenNode.  
In "File structure" section explain all file definetion, find out the "CO_driver_target.h":

* CO_driver_target.h - Example hardware definitions for CANopenNode.
* CO_driver_blank.c - Example blank interface for CANopenNode.

CANOpenNode stack provides uC demo for PIC/STM32, but there is not Arduino demo.  
The basic CANOpenNode stack includes the CAN message process for CANOpen, but the code of hardware control needs implemented by the developer to fit the varying platform.
