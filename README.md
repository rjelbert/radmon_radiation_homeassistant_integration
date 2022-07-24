# radmon_radiation_homeassistant_integration

This is work in progress. Various ways to integrate data from www.radmon.org into Home Assistant (HA)

24th July 2022

The first file is yaml config data that adds radmon data as a command line type HA sensor
You'll need to paste this code into your main HA config file and restart HA
I have added a few additional statistical sensors to generate 10 minute and 30 minute average versions
You will need to edit the Entity settings manually to change the icon types to mdi:radioactive


TODO (if I get time):

Make the config use current location to select the nearest radmon station automatically

Make the icon state update for when the sensor is down / stopped providing updates

Expose the last updated time/date stamp
