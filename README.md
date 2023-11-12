# Environmental Sensor Data Collector with LoRaWAN

## Description

This project involves collecting environmental data using BMP280 and HDC1080 sensors and transmitting it over a LoRaWAN network. It's designed for applications in remote monitoring of environmental conditions such as temperature, humidity, and air pressure.

## Features

- Data collection from BMP280 (temperature and air pressure) and HDC1080 (temperature and humidity) sensors.
- LoRaWAN communication for efficient and long-range data transmission.
- Power management for sensors to optimize battery usage.

## Hardware Requirements

- SCT6201H board

## Software Dependencies

- `Wire.h`: Standard Arduino library for I2C communication.
- `BMP280.h`: Library to interface with the BMP280 sensor.
- `HDC1080.h`: Library to interface with the HDC1080 sensor.
- `LoRaWan_APP.h`: Library for handling LoRaWAN communication.

## Installation

1. Install Arduino IDE and necessary drivers for your microcontroller.
2. Connect your microcontroller to your computer.
3. Open the Arduino IDE and install the `BMP280` and `HDC1080` libraries through the Library Manager.
4. Copy the provided code into a new sketch in the Arduino IDE.
5. Select the correct board and port from the Tools menu.
6. Compile and upload the sketch to your microcontroller.

## Usage

After setting up and powering on your device, it will automatically start collecting data from the sensors and transmitting it over LoRaWAN. 

- `power_On_Sensor_Bus()`: Power on the sensor bus for data collection.
- `hdc1080_fetch()`: Fetch data from the HDC1080 sensor.
- `bmp280_fetch()`: Fetch data from the BMP280 sensor.
- `prepareTxFrame(uint8_t port)`: Prepares the LoRaWAN data packet for transmission.

## Configuration

- Set LoRaWAN OTAA parameters (`devEui`, `appEui`, `appKey`) as per your network provider's specifications.
- Configure ABP parameters (`nwkSKey`, `appSKey`, `devAddr`) if using ABP mode.
- Adjust `loraWanRegion` and `loraWanClass` according to your geographical location and class of device.

## Troubleshooting

- Ensure all connections to sensors are secure.
- Verify that the correct libraries are installed.
- Check the serial monitor for any error messages or debugging information.

## License

This project is released under the MIT License.

## Acknowledgments

Thanks to the Arduino community for providing extensive resources and libraries which made this project possible.
