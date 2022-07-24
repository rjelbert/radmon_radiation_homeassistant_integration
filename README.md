# radmon_radiation_homeassistant_integration

This is work in progress. Various ways to integrate data from www.radmon.org into Home Assistant (HA)


24th July 2022

The first file is yaml config data that adds radmon data as a command line type HA sensor
You'll need to paste this code into your main HA config file and restart HA
I have added a few additional statistical sensors to generate 10 minute and 30 minute average versions
You will need to edit the Entity settings manually to change the icon types to mdi:radioactive


Misc radiation notes:

CPM (or counts per minute) are the events counted from a Geiger Muller (GM) Tube during a one minute period and is usually used
to calculate a radiation level. See https://en.wikipedia.org/wiki/Geiger%E2%80%93M%C3%BCller_tube

Different GM Tubes have different sensitity levels and therefore produce different CPM for the same radiation levels. For example, some GM tubes produce 0-5 CPM and others 50-100 CPM for the same background radiation level. 

For the examples on this github project, I use 0.00812037 as the conversion factor to convert to uSv/h because my rjelbert station has a J305 GM tube. 

See https://en.wikipedia.org/wiki/Sievert

See your GM tube datasheet for an individual conversion factor for the radmon station you select. Also read https://www.pascalchour.fr/ressources/cgm/cgm_en.html 

Note that most people stick with the CPM values and learn what normal looks like by looking at the data.


What various levels might mean (from various google searches):

0.27µSv/h - Typical background level

1.14µSv/h - Shelter population

5.7µSv/h  - Evacuation of population

11.4µSv/h - Issue Iodine tablets

https://xkcd.com/radiation (for an interesting chart on dose levels)

https://en.wikipedia.org/wiki/Ionizing_radiation



TODO (if I get time):

Make the config use current location to select the nearest radmon station automatically

Make the icon state update for when the sensor is down / stopped providing updates

Expose the last updated time/date stamp

Add a uSv/h conversion sensor
