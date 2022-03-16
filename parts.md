# Parts

### Peripherals
- Smart Lamp: [LIFX white e26 smart bulb](https://www.lifx.com/products/lifx-white)
- light sensor: [Adafruit BH1750](https://www.adafruit.com/product/4681)
- Bluetooth module: [DSD Tech HC-05](https://www.amazon.com/gp/product/B01G9KSAF6/ref=ox_sc_act_title_3?smid=AFLYC5O31PGVX&psc=1)

### Serial Interfaces
- I2C: Used to retrieve the luminance data measured by the BH1750 sensor.
- UART: Used to broadcast the calculated bulb brightness data to the Python script, which then sends a state change request to the bulb.
