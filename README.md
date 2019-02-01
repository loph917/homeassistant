# homeassistant
my contributions to home assistant

## ecobee.py
this is a replacement for the original ecobee.py that corrects the reporting of thermostat operational STATE (not MODE). the original ecobee.py component does get the current STATUS of the equipment and puts it into an attribute (*operation*) but it does not use it in any meaningful way. 

### my interpretation of MODE and STATE:
..* MODE is the current operational setting as selected by the user. it can be heat, cool, auto, auxHeatOnly or off (per the ecobee api).
..* STATUS (ecobee api call for EquipmentStatus) is the current operation of the equipment as determined by the thermostat. it is possible for the MODE to be set to one of the above modes but the system is in an IDLE status because the demand for heating or cooling has been satisfied (which is determined by the user defined/pre defined setpoint temperature(s)).

### installation
instead of using a custom component i chose to replace the existing ecobee.py which is shipped as part of ecobee. yes this means every time you upgrade homeassistant you'll need to deal with this file.

install the new ecobee.py into components/climate directory of your homeassistant installation.

example: if your homeassistant is installed in /srv/homeassistant then the replacment ecobee.py file would go into /srv/homeassistant/lib/python3.5/site-packages/homeassistant/components/climate

[logo]: images/thermostat02.png "incorrect example"