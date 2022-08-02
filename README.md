# INTERNET-OF-THINGS
0.    https://wokwi.com/projects/333797120426377810      (************)
0.    https://wokwi.com/projects/333800186223526484      (************)
0.    https://wokwi.com/projects/335070683477312084      (*************)
0.    https://wokwi.com/projects/335069692992422482      (************)


1.    https://wokwi.com/projects/333802921425633876      (RGB TRAFFIC LED)
2.    https://wokwi.com/projects/333804671527289428      (RGB  MULTICOLOR LED)
3.    https://wokwi.com/projects/334980963080602194      (servomotor clock type)
3.    https://wokwi.com/projects/334980924249735764      (servomotor 2)
4.    https://wokwi.com/projects/334982095306752595      (servometer with potentiometre)
5.    https://wokwi.com/projects/335705347315466835      (servomoter with pushbutton)
6.    https://wokwi.com/projects/335611961780732498      (lcd-hello wokwi)
7.    https://wokwi.com/projects/335065041687544403      (buzzer with resistor)
8.    https://wokwi.com/projects/335065955278258772      (buzzer with pushbutton)
9.    https://wokwi.com/projects/335071500453282387      (ultrasonic sensor)
10.   https://wokwi.com/projects/335605272348197460      (ultrasonic with buzzer)
11.   https://wokwi.com/projects/335611600253747796      (ultrasonic sensor with led and buzzer)
12.   https://wokwi.com/projects/335616252190917203      (two ultrasonic with two buzzer)
13.   https://wokwi.com/projects/335701664758497874      (potentiometer with led)
14.   https://wokwi.com/projects/336881829987484242      (ESP 32)  
**HARDWARE:-**
1.   https://wokwi.com/projects/338227139367141971      (1. to turn LED on for 1 sec after every 2 sec)
2.   https://wokwi.com/projects/338226711455859284      (2. turn on the LED when pushbutton is pressed)
3.   https://wokwi.com/projects/338147082096345683      (DHT22 humidity sensor with temperature)
4.   https://wokwi.com/projects/335705347315466835      (servomoter with pushbutton)
5.   https://wokwi.com/projects/338154081559249491      (DHT22+LCD)


int red = D1;
 int green = D6;
 int blue = D7;
 //GROUND IS CONNECTED TO 3V 
 void setup() {
   pinMode(red, OUTPUT);
   pinMode(green, OUTPUT);
   pinMode(blue, OUTPUT);

 }

 void loop() {
   displayColor(0b100); //RED
   delay(1000);
   displayColor(0b010); //GREEN
   delay(1000);
   displayColor(0b001); //BLUE
   delay(1000);
   displayColor(0b101); //MAGENTA
   delay(1000);
   displayColor(0b011); //CYAN
   delay(1000);
   displayColor(0b110); //YELLOW
   delay(1000);
   displayColor(0b111); //WHITE
   delay(1000);
 }

 void displayColor(byte color) {
   digitalWrite(red, !bitRead(color, 2));
   digitalWrite(green, !bitRead(color, 1));
   digitalWrite(blue, !bitRead(color, 0));
 }
