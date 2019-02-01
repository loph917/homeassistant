# homeassistant
my contributions to home assistant

ecobee.py - this is a replacement for the original ecobee.py that corrects the reporting of thermostat operational state. my interpretation of the MODE and STATE:
- MODE is the current operational setting as selected by the user. it can be heat, cool, auto, auxHeatOnly or off (per the ecobee api).
- STATUS (ecobee api call for EquipmentStatus) is the current operation of the equipment as determined by the thermostat. it is possible for the MODE to be set to one of the above modes but the system is in an IDLE status because the demand for heating or cooling has been satisfied (which is determined by the user defined/pre defined setpoint temperature(s)).
