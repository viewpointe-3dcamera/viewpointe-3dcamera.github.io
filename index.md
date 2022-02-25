# ECE 153B - Energy Efficient Lighting

### Overview/Goal/Purpose:
We would like to create a energy efficient lighting system, that will only draw as much power as is absolutely needed. To do this, we will implement a light sensor, which will monitor the ambient light of the space and make adjustments in the LED brightness to maintain a standard level of overall brightness in the space. A secondary goal to further conserve energy is to implement motion or infrared based triggering, so the light only turns on once there is someone in the vicinity, and turns off once they leave.

### Peripherals
- LED/smart lamp or dimmer switch: LIFX white e26 smart bulb
- light sensor: adafruit bh1750
- optional motion/infrared sensor: onyehn infrared pir motion sensor detector

### Serial Interfaces
- I2C (Light sensor)
- UART (To python script used to control light bulb)

### Software Structure
If implementing motion detector: From an idle state, system is "woken up" by an interrupt triggered by the pulse from motion sensor.

If manual wake: Simply powering on the circuit will let the system enter a monitoring state.

The system, when awake, will take continuous readings from the light sensor, and use the comparison of this lux value to determine how much the bulb should be adjusted. This is sent via UART to a Python script (do we need a bluetooth module here?), which then uses the LIFX API to control the brightness of the bulb, adjustable by percentage.

### Weekly Updates
**02/25:**
We bought the LIFX Smart Lamp and worked on interfacing with the LIFXLAN library to control the lamp with Python. We also worked on setting up the BH1750 sensor using I2C protocols, by pseudocoding all the functions (init, reset, mode set, read data, etc) and understanding the commands taken by the sensor. We referenced Lab 4's I2C setup to do this. We will also be ordering the motion sensor.

## Using Github pages (reference)

You can use the [editor on GitHub](https://github.com/kthanigaivelan/ece_153b_project/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# does this work?
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/kthanigaivelan/ece_153b_project/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
