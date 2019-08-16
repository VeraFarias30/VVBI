# VVBI
SENSOR DE HUMEDAD Y PANTALLA
#include <DHT.h>
#include <DHT_U.h>

#include <DHT.h>
#include <DHT_U.h>

#include <DHT.h>
#include <Wire.h>
#include <LCD.h>
#include <LiquidCrystal_I2C.h>
#define DHTPIN 4
#define DHTTYPE DHT11
DHT dht (DHTPIN,DHTTYPE);

int x = 200;
int y = 300;
//creamos el objeto display LCD I2C
LiquidCrystal_I2C LCD(0X3F, 2, 1, 0, 4, 5, 6, 7, 3, POSITIVE);
// Addr, En, Rw, Rs, d4, d5, d6, backlighpin, polarity

void setup () 
{
  dth.begin ();
  lcd.begin (16,2);
  // lcd.backlight();
  lcd.setCursor(0, 0);
  lcd.print("primera fila");
  lcd.setCursor(0, 1);
  lcd.print("sgunda fila");
  delay (3000);
  lcd.clear

 lcd.setCursor(10, 0);
 lcd.print("HOLA");
 lcd.setCursor(10, 1);
 lcd.print("ADIOS");
 delay (3000);
 lcd.clear();

 lcd.setCursor(0,0);
 for(int x=0; x<10;x++)
 
 {
  lcd.print(x);
 delay(500);
 lcd.clear()
  
  }
  for(int x=0 x<10;x++)
  {
    lcd.print("vvbi  );
    delay(300);
    lcd.clear();
    delay(300);
    
  }

  lcd.print("  arduino   ");

  for(int x=0 x<5;x++)

{
  lcd.scrollDisplayLeft();
  delay(300):
  
}

 for(int x=0; x<9;x++)

 {
  lcd.scrollDisplayRight();
  delay(300);
  
 }
lcd.clear();
lcd.print("   ARDUINO   ");

}

void loop()
{
  int h= dht.readHumidity();
  int t= dht.readTemperature();
  lcd.setCursor(0,0);
  lcd.print("TEMPERATURA:");
  lcd.setCursor(0, 14);
  lcd.print(t);
  lcd.setCursor(1, 10);
  lcd.print("HUMEDAD:"),
  
  lcd.setCursor(1, 10);
  lcd.print (h);
  delay(1500);
  
}
