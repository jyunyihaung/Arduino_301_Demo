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

##


