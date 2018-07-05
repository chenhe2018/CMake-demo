# choose when compile

>cd build

>ccmake ..

>make

## WAINING

Because we use "build" directory for compiling results, so the 'config.h' will be generated there. So, main.cc should #include"build/config.h".
