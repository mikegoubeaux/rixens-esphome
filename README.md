# Rixen's ESPHome for Home Assistant
ESPHome YAML for Rixen's **MCS7** Hydronic Heating System

## Disclaimer

This configuration is offered as-is and for free. **USE AT YOUR OWN RISK**.

## Overview

This [ESPHome](https://esphome.io) YAML is written for an esp32 and uses the [esp32_can CAN Bus platform](https://esphome.io/components/canbus.html#esp32-can-component).

This is written and tested for the [Rixen's MCS7 hardware](https://rixens.com/collections/mcs-7-hydronic-system-documents). The CAN interface is pointed out on page 10 of the Rixen's [MCS7 Installation Manual](https://rixens.com/collections/mcs-7-hydronic-system-documents).

**NOTE:** This configuration assumes the presence of the engine preheat loop AND pump. To successfully use this configuration, you will very likely need to make modifications. See notes below.

![Screenshot 2024-01-31 at 10 08 05 AM](https://github.com/mikegoubeaux/rixens-esphome/assets/9661510/394ea22f-41c4-4714-8a11-c7cb545bdce4)

![Screenshot 2023-11-06 at 1 32 22 PM](https://github.com/mikegoubeaux/rixens-esphome/assets/9661510/dfb0d1ca-18c2-4d9b-b036-19ced3874270)

### Customization

Please keep in mind this YAML is intended to serve as an example and will likely need modified for your specific use case.

For instance, this configuration imports a sensor from Home Assistant that overrides the hardwired D+ signal into the Rixen's control unit to indicate the engine is running. Additionally, there is logic that may not be desireable in your use case.

It is also important to note that although this configuration creates a Climate Thermostat, it is not actually being used for hysteresis or to make the call for heat. The Rixen's control box manages the call for heat. The Climate entity created serves primarily to establish a target temperature and to provide a visual interface in Home Assistant. The various heat source switches are bi-directional; if they are adjusted on the Rixen's control interface, the changes will be reflected in Home Assistant. So, you can use either or both methods of control.

## Pinouts

The CAN Bus pins are not labeled on the Rixens' control module. Here is a diagram of the pins. You can double check your pin out by metering the pins for 12v, ground, and CAN bus voltages. CAN Hi usually measures from 2.5V to 3.75V while CAN Lo measures from 2.5V to 1.25V.

<img width="562" alt="Rixens CAN bus pinout" src="https://github.com/mikegoubeaux/rixens-esphome/assets/9661510/9141288c-cbe0-469c-b7b9-9b02a6126366">
