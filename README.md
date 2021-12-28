# UNOFICIAL CUSTOMIZATION OF THIRD PARTY LIBRARY
With this library you can use the LiquidCrystal_I2C library with Arduino Nano 33 IOT and avoid AVR architecture related compilation errors.

Pinout wich I used for Nano 33 IOT: SDA -> A4, SCL ->A5.

## Changes to make it compatible (LIQUIDCRYSTAL_I2C/LiquidCrystal_I2C.h):
51 // Version 1.1.4 for AVR architectures 
52 //#define En B00000100  // Enable bit
53 //#define Rw B00000010  // Read/Write bit
54 //#define Rs B00000001  // Register select bit

56 // Version 1.1.5 for AVR architectures by Sergio Forcen <sforceas@gmail.com>
57 #define En 0b00000100  // Enable bit
58 #define Rw 0b00000010  // Read/Write bit
59 #define Rs 0b00000001  // Register select bit

Updated En, Rw and Rs values to compatible ones, following the compiler debugger suggestions.

# LiquidCrystal_I2C

LiquidCrystal Arduino library for I2C LCD displays

**Status: Archived** 
This repository has been transfered to GitLab at https://gitlab.com/tandembyte/LCD_I2C
