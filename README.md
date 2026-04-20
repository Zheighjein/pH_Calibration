pH Calibration for Gravity Analog pH Sensor Kit V2 (DFRobot)

Microcontroller : Raspberry Pi 4

Analog to Digital using ADS1115 board

Install Dependency

pip install adafruit-circuitpython-ads1x15


BEFORE RUNNING

1. sudo raspi-config   # enable I2C
2. i2cdetect -y 1      # should show 0x48
#==== TO CHECK I2C ===IT SHOULD SHOW 48
pi@raspberrypi:~ $ i2cdetect -y 1


3. pip3 install adafruit-circuitpython-ads1x15


HOW TO RUN

1. Run script
2. Put probe in pH 7 → wait ~10 seconds → press ENTER
3. Rinse probe (important)
4. Put probe in pH 4 → wait ~10 seconds → press ENTER
5. Done ✅ (auto-saved)
6. Next runs = instant readings


# =========================
# RASPBERRY PI → ADS1115
# =========================

Pi 3.3V (Pin 1)  -------->  VDD (ADS1115)
Pi GND (Pin 6)   -------->  GND (ADS1115)

Pi SDA (GPIO2, Pin 3) --->  SDA (ADS1115)
Pi SCL (GPIO3, Pin 5) --->  SCL (ADS1115)

# Optional (usually not needed)
ADDR → GND (default I2C address 0x48)


# =========================
# ADS1115 → pH SENSOR
# =========================

A0 (ADS1115)     -------->  PO (pH sensor analog output)

# =========================
# POWER FOR pH SENSOR
# =========================

Pi 5V (Pin 2 or 4) ------>  VCC (pH sensor)
Pi GND (Pin 9)   -------->  GND (pH sensor)







