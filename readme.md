[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg)](https://github.com/custom-components/hacs)

# Lovelace Bus Card 

This Lovelace custom card displays Bus data from the public api for a given stop and route.

This is designed to work with the translink sensor: https://github.com/wymanhns/HKBUS-Sensor

![Preview](https://github.com/wymanhns/bus-card/blob/main/BUS_Card.png?raw=true)



### Manual install
1. Download and copy 'bus-card.js' into your 'config/www' directory.

2. Add a reference to 'mini-graph-card-bundle.js' inside your 'ui-lovelace.yaml' or at the top of the *raw config editor UI*:

```yaml
resources:
  - url: /local/bus-card.js
    type: js
```

### HACS Custom Install

1. Go to the community tab of your home assistant installation
2. Click settings
3. Add "https://github.com/wymanhns/bus-card" with the type **Plugin**
4. Click Save

###  Using the card

Add the following lines to your ui-lovelace.yaml (entity should be the ids of translink sensors):

```yaml
cards:
  - type: custom:bus-card
    entities:
      - entity: sensor.hk_bus_43a
      - entity: sensor.hk_bus_248m

```
