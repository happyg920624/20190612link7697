*序列埠(Serial Port)
#include <LiquidCrystal_I2C.h>
LiquidCrystal_I2C lcd_i2c(0x3F);

#include <DHT.h>

DHT dht11_p2(2, DHT11);

void setup()
{
  lcd_i2c.begin(16, 2);

  dht11_p2.begin();
  Serial.begin(9600);

}


void loop()
{
  Serial.println(dht11_p2.readHumidity());
  delay(200);
  Serial.println(dht11_p2.readTemperature());
  delay(200);
if (false) {

} else {

}

}
