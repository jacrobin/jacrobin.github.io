---
title: "One Day Build (ODB) #1: Temperature & Humidity Sensor Part: i"
date: 2023-07-19T14:15:56-07:00
draft: false
ShowToc: true
TocOpen: true
---

# Intro:
This is a new thing I want to start doing where I try to build something at least once a month, and within a day (ideally). To kick things off I wanted to test, and build, a simple arduino powered temperature and humidity sensor. This overall took about three hours including testing of planning, sensors, wiring, testing, and coding. 

# Build Overview:

The build needed to meet two criteria:
- Read both humidity and temperature reliably
- Be able to connect to a RaspberryPi later (Part: ii)

To meet these criteria an Arduino was used. While a RaspberryPi alone could have been used, the added complexity of separate system communication had more appeal.

### Components Used

| Part        | Description |
| ----------- | ----------- |
| ELEGOO UNO R3 | Single-board microcontroller |
| Generic LCD 16x2 Screen   | Shows up to 32 characters. Gives immediate readable data.|
| IC2 Adapter | Simplifies wiring and control for the LCD display. |
| DHT11 | Three pin variant of DHT temperature & humidity Sensor |
| 2 x LED | Show state of executed code|

### Final Result

See companion [code here](https://github.com/jacrobin/arduino-temp-and-humidity/blob/main/temp-humid-lcd.ino). The design is very basic, and is nothing new. There exists a miriad of setups like this online, and is only intended to setup the ground work for part ii. The added step of adding heat-shrink did make the  build overall look and feel more stable.

![a](/images/main-view.png#center)
![a](/images/view-working.png#center)

# Whats Next?

![a](/images/flowchart.svg#center)

The next step is to, ideally, pull local weather data from the internet, and have a website hosted locally that shows all relevant data into a single landing page. I have not done any research on free-ish api's or data I can pull from but there are a few things I want to gather if possible:

### Desired Data Points: 

- Radar.
- Local temperature and humidity (as close to my house as possible).
- General air quality.
- Wind speed and direction.
- Moon phase.

Another goal of part ii is to employ NASA's [The Power of 10: Rules for Developing Safety-Critical Code](https://en.wikipedia.org/wiki/The_Power_of_10:_Rules_for_Developing_Safety-Critical_Code). While the code written in the following phases will not be considered critical, the challenge of following these rules seems interesting.

# Takeaways:

- IC2 adapters are awesome. Easy to solder, cheap, and they make the process of interfacing with LCD screens like these much easier. I highly recommend them, especially if they are preinstalled.
- The DHT senor seems to fail every 30 readings or so. I am not sure why. But with limited testing it seems to be reliable enough for it's purpose. Additionally, I compared the ambient readings with a store bought thermostat and humidity reader. The humidity was identical, but the temperature seemed always off +/- one degree. A tolerance I am more than willing to accept. 
