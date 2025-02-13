# Vindriktning with Esphome
(forked from https://github.com/sharandac/vindriktning)


Let's make the Ikea Vindriktning air quality sensor a little smarter. Here is the matching completely over-engineered firmware.

## prerequisite

ESP32 - S2 mini (any ESP32/ESP8266 would work, but i had these lying around)<br>
Ikea Vindriktning<br>
PH0 Philips Screwdriver (long-ish)

# Install


## hardware modification in 4 steps

esp32 -> Vindriktning:<br><br>
VCC -> +5V<br>
GND -> GND<br>
GPIO17 -> reset<br>

![step 1](images/IMG_20230311_173537.jpg)
![step 3](images/IMG_20230311_173259.jpg)
![step 4](images/IMG_20230311_173308.jpg)
![step 2](images/IMG_20230311_173335.jpg)

## Esphome
Flashing is easy, add your wifi credentials to the yml file and run:
```
esphome run esp_ikea.yml
```

For the ESPS2mini you need to press the buttons RST + BOOT together, then release the RST button to enter boot mode.

## Integration in Homeassistant
Once flashed you will find the sensor within homeassistant's esphome integration (add new instance with the IP address of the just flashed device)


# Contributors

Every Contribution to this repository is highly welcome! Don't fear to create pull requests which enhance or fix the project, you are going to help everybody.
<p>
If you want to donate to the author then you can buy me a coffee.
<br/><br/>
<a href="https://www.buymeacoffee.com/sharandac" target="_blank"><img src="https://img.shields.io/badge/Buy%20me%20a%20coffee-%E2%82%AC5-orange?style=for-the-badge&logo=buy-me-a-coffee" /></a>
</p>
