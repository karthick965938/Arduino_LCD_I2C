# Arduino with LCD Display(I2C Module)

Here i have list down simple steps for connect ***Arduino with LCD Display***

> I have used two basic library

- Wire(This is default one)
- [LiquidCrystal_I2C](https://github.com/karthick965938/Arduino_LCD_I2C/tree/master/Arduino-LiquidCrystal-I2C-library/) (click this link to download)

Once you have install above libraries. First you can check simple code which is i have added below :) (copy and paste on your Arduino Compiler). If you have ran compiler successfully you can upload your code on Arduino Board.
```
#include <Wire.h> 
#include <LiquidCrystal_I2C.h>
//I2C pins declaration
LiquidCrystal_I2C lcd(0x27, 16, 2);
void setup() 
{
  lcd.begin();//Initializing display
  lcd.backlight();//To Power ON the back light
  //lcd.backlight();// To Power OFF the back light
}
void loop() 
{
  lcd.clear();// Clear your screen
  lcd.setCursor(0,0); //Defining positon to write from first row,first column .
  lcd.print("Spritle Tech"); //You can write 16 Characters per line .
  delay(1000);//Delay used to give a dynamic effect
  lcd.setCursor(3,1);  //Defining positon to write from second row,first column .
  lcd.print("Karthick Nagarajan");
}
```

***This is Actul circuit connection. I hope this will help on how to wiring.***

![circuit](https://github.com/karthick965938/Arduino_LCD_I2C/blob/master/circut.png)
