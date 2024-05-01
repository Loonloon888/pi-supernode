[![Lint Code Base](https://github.com/KOSASIH/pi-node/actions/workflows/super-linter.yml/badge.svg)](https://github.com/KOSASIH/pi-node/actions/workflows/super-linter.yml)
[![CI](https://github.com/KOSASIH/pi-node/actions/workflows/blank.yml/badge.svg)](https://github.com/KOSASIH/pi-node/actions/workflows/blank.yml)

# pi-node

This repository contains the source code for a simple Node.js application that runs on a Raspberry Pi. The application listens for incoming HTTP requests and responds with a message indicating the current temperature and uptime of the Raspberry Pi.

# Prerequisites

To run this application, you will need the following:

1. A Raspberry Pi with Node.js installed
2. A temperature sensor (such as a DS18B20) connected to the Raspberry Pi

# Getting Started

1. Clone this repository to your Raspberry Pi:

```
git clone https://github.com/KOSASIH/pi-node.git
```
2. Install the required dependencies:

```
cd pi-node
npm install
```

3. Edit the config.js file to specify the temperature sensor's device file path. For example, if you're using a DS18B20 connected to GPIO pin 4, the device file path will be /sys/bus/w1/devices/28-000005f8b8ff/w1_slave.

4. Start the application:

```
npm start
```
5. Use a web browser or a tool like curl to send an HTTP request to the Raspberry Pi and view the response:

```
curl http://<RASPBERRY_PI_IP_ADDRESS>:3000
```
The response will look something like this:
```
Temperature: 23.5°C, Uptime: 1 day, 2 hours, 34 minutes, 56 seconds
```

# License

This project is licensed under the MIT License - see the LICENSE.md file for details.
