# homeassistant
my contributions to home assistant

ecobee.py - this is a replacement for the original ecobee.py that corrects the reporting of thermostat operational state.
- MODE is the current operational setting as selected by the user. it can be heat, cool, auto, auxHeatOnly or off (per the ecobee api).
- STATUS (api call for EquipmentStatus) is the current operation of the equipment as determined by the thermostat. it is possible to be set for HEAT or COOL but the system is actually in an IDLE status because the demand for heat or cool has been satisfied which is defined by the user defined setpoint temperature.
