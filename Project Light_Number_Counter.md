# Project Light_Number_Counter
### Created by Kien Le Trung and Timur Garifullin

## Criteria A: Planning
### Context of the product
We are creating a product that can counts number from 0 to 9. It will shows different combinations of LEDs when customers click different combinations of buttons. Our product's body will be created from wood.

#### Sketches of Ideas
![](https://github.com/BrightChanges/Unit-2/blob/main/IMG_3803_new.jpeg)
Fig.1 Our sketch for how the buttons will turn on the lights and values associate with the lights


## Criteria B: Design
#### System Diagram

![](https://github.com/BrightChanges/Unit-2/blob/main/System%20diagram%20Hand%20project.png)
Fig.2.1 The neat and clean system diagram of our program

![](https://github.com/BrightChanges/Unit-2/blob/main/IMG_3827.JPG)
Fig.2.2 The sketchy ystem digram of our program


#### Flow Diagram
![](https://github.com/BrightChanges/Unit-2/blob/main/Project%20Light_Number_Counter_Kien%20and%20Timur%20(2).png)

Fig.3 Flow diagram of how the action of pushing buttons will turn on the light

#### Truth tables/ K-maps
![](https://github.com/BrightChanges/Unit-2/blob/main/IMG_3807.jpg)

Fig.4 Truth tables of our program

![](https://github.com/BrightChanges/Unit-2/blob/main/IMG_3808.JPG)
Fig.5 K-maps of our program


## Criteria C: Development
1st development story:
-First, we, Timur and I, tried to codes right after we finished drawing the product's sketches, flow diagram, truth table. However, we realized that we will need to write 9 if statements for the codes to work. So we then draw the K-maps to generate our product's system's boolean logic. We were then able to use the boolean logic to write our codes with 6 boolean statements. (not significantly less but lesser codes are alway better :) Our codes are shown below:

#### Codes

```.py
//All the int ... codes below register the port (the ports on Arduino) of each button and light 
int button_x_port = 4; 
int button_y_port = 5; 
int button_z_port = 6; 
int button_w_port = 7; 

int light_a = 13;
int light_b = 8;
int light_c = 9;  
int light_d = 10;
int light_e = 11;
int light_f = 12;

int button_x_value = 0;
int button_y_value = 0;
int button_z_value = 0; 
int button_w_value = 0;

//The codes below set up the OUTPUT of our devices, which are the 6 lights (a,b,c,d,e,f)
void setup()
{
  pinMode(light_a, OUTPUT);
  pinMode(light_b, OUTPUT);
  pinMode(light_c, OUTPUT);
  pinMode(light_d, OUTPUT);
  pinMode(light_e, OUTPUT);
  pinMode(light_f, OUTPUT); 
  Serial.begin(9600);
}

//The codes in the void loop () contains the boolean logic behind different combinations of buttons and lights/LEDs.
void loop()
{
  //The codes below read the INPUT from the 4 buttons
  button_x_value = digitalRead(button_x_port);
  button_y_value = digitalRead(button_y_port);
  button_z_value = digitalRead(button_z_port);
  button_w_value = digitalRead(button_w_port);
 
 //The codes below show the boolean logic of each light (a,b,c,d,e,f)
 //a
 int eq_a = ((!button_y_value)&&(!button_z_value)&&(!button_w_value))||((button_x_value)&&(!button_y_value)&&(!button_z_value))||((!button_x_value)&&(button_y_value)&&(button_z_value));
  digitalWrite(light_a,eq_a);
 //b
 int eq_b = ((button_x_value)&&(!button_y_value)&&(!button_z_value))||((!button_x_value)&&(button_y_value))||((!button_x_value)&&(!button_y_value)&&(button_w_value))||((!button_x_value)&&(!button_y_value)&&(button_z_value));
  digitalWrite(light_b,eq_b);

  
 //c
 int eq_c = ((!button_x_value)&&(button_y_value)&&(!button_z_value))||((button_x_value)&&(!button_y_value)&&(!button_z_value))||((!button_x_value)&&(!button_y_value)&&(button_z_value))||((!button_x_value)&&(button_y_value)&&(button_w_value));
 digitalWrite(light_c,eq_c);

 //d
 int eq_d = (!button_x_value)&&(button_y_value)&&(!button_z_value)||(button_x_value)&&(!button_y_value)&&(!button_z_value)||(!button_x_value)&&(!button_y_value)&&(button_z_value)&&(button_w_value);
 digitalWrite(light_d,eq_d); 

 //e 
 int eq_e = (!button_x_value)&&(button_y_value)&&(!button_z_value)||(button_x_value)&&(!button_y_value)&&(!button_z_value)&&(button_w_value);
 digitalWrite(light_e,eq_e); 
 
 //The Serial.print codes are used for checking if our codes are working
 //f                    
 int eq_f = (!button_x_value)&&(button_y_value)&&(!button_z_value)&&(button_w_value);
 digitalWrite(light_f,eq_f);  
 Serial.print(eq_a);
 Serial.print(eq_b);
 Serial.print(eq_c);
 Serial.print(eq_d);
 Serial.print(eq_e);
 Serial.println(eq_f); 
}


```
2st development story: After finishing writing the codes, we started to assemble our product based on the model we created on Tinkercard (the image of it is shown below). During the process, we met difficulties in connecting the LEDs with the resistors because we didn't use soldering devices. However, we were able to overcome this by bending the LEDs and resistors' knees and stick them with tape. Our assembled or final product is shown in Criteria D below.

![](https://github.com/BrightChanges/Unit-2/blob/main/Screen%20Shot%200002-11-22%20at%202.42.43%20PM.png)
Fig.6 Our product's model on Tinkercad

## Criteria D: Functionality
#### Real-life program
Link to the desmontration video (without the wood hand): https://github.com/BrightChanges/Unit-2/blob/main/IMG_3819.MOV

Picture of our program (with wood hand):

![](https://github.com/BrightChanges/Unit-2/blob/main/IMG_3857.JPG)
Fig.7 Front side picture of our program


![](https://github.com/BrightChanges/Unit-2/blob/main/IMG_3858.JPG)
Fig.8 Back side picture of our program

![](https://github.com/BrightChanges/Unit-2/blob/main/Number_counter%20(1).png)
Fig.9 Instruction table showing customer how the LEDs are shown and which buttons to press to show them.

##### Link to desmonstration video (with wood hand) in the light: https://github.com/BrightChanges/Unit-2/blob/main/IMG_3855.MOV

##### Link to desmonstration video (with wood hand) in the dark: https://github.com/BrightChanges/Unit-2/blob/main/New_CS.mov

## Criteria E: Evaluation
| Test                                                                                          | Expected Outcome                                                                                                                                                                                                                   | Met?          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| Criteria 1: See if our product count number 0-9.                                              | If you pressed the button's combination for a number,  the display shows a pattern for that number  (customers can do this while looking at our  "Button Operation Table") Ex: Click no buttons-> no light turned on (value=0); Click the green button-> turn on 1 light (value=1); Click the red button-> turn on 2 lights (value=2)... |   Yes            |
| Criteria 2: See if we provided you with a table showing LED  sequences for each number 0-9    | You are able to see a table showing patterns of LEDs for each number 0-9 that is  presented.                                                                                                                                       |       Yes        |
| Criteria 3: See if we provided you with a table showing buttons sequences for each number 0-9 | You are able to see a table showing patterns of buttons (4 buttons with 4 colors: yellow, blue, red, green) for each number 0-9 that is presented.                                                                                                                                     |       Yes        |
| Criteria 4: Check if our product uses maximum of 7 LEDs and 4 buttons.                        | You will see that our product uses no more than 7 LEDs  and 4 buttons.                                                                                                                                                             |   Yes            |
| Criteria 5: See if our product contains a wood-body.                                          | You will see that our product's body is created from wood.                                                                                                                                                                         |    Yes           |
#### Success Criteria
1. The display should count from 0-9.
2. A table showing each number 0-9 and the corresponding LEDs is included.
3. A table showing the operation of the buttons and number 0-9 is included.
4. The display was maximum 7 LEDs and 4 buttons.
5. The main body of the project is made out of wood with the help of laser cutter.

