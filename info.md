# Lovelace Bus Card 

This Lovelace custom card displays Bus data from the public api for a given stop and route.

This is designed to work with the translink sensor: https://github.com/wymanhns/HKBUS-Sensor

![Preview](https://github.com/wymanhns/bus-card/blob/master/BUS_Card.png?raw=true)

###  Using the card

Add the following lines to your ui-lovelace.yaml (entity should be the ids of translink sensors):

```yaml
cards:
  - type: custom:bus-card
    entities:
      - entity: sensor.hk_bus_43a
      - entity: sensor.hk_bus_248m
```