# Mars_task2
recruitment task2

Aim:-Make an object counter, which usesan IR sensor to count the number ofpassing objects and displays thecount on an LCD screen.

Components used:- Lcd display , i2c , ir sensor module, arduino uno board , jumper wires

Thought Process:- As i am using a IR sensor, so it will detect the object that passes by, and it will be stored in the variable. It will not count the second object till the first object is passed from the sensor and second one  is detected. For this purpose I had to use another variable which will keep track that first object is removed or not. The data need to be displayed on the lcd diplay so i had to to include the lcd initialisation in the code.
so the concept is as any object is detected through the sensor its turn low, and the variable for tracking the object change ( state) ( initialy it is = true ) both are 1 then the object is counted and state is changed to false. now it will not turn the state value to true till the ir sensor value is high. If the ir sensor value is high then it enters int the if loop and changes state to true. the process goes on and the count value increses with it 

There was one error coming while interfacing the code for lcd display with i2c 
errors:-
'lcd' was not declared in this scope lcd.init();  
it was because i was using wrong initialisation ((LiquidCrystal_I2C.h lcd(0x27,16,2)) but the correct one is (LiquidCrystal_I2C lcd(0x27,  16, 2))

References :-
https://projecthub.arduino.cc/arduino_uno_guy/i2c-liquid-crystal-displays-5eb615

https://techatronic.com/object-counter-using-ir-sensor-and-arduino/ 



