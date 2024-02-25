# Rixen's ESPHome for Home Assistant
ESPHome YAML for Rixen's **MCS7** Hydronic Heating System

## Notes
This [ESPHome](https://esphome.io) YAML is written for an esp32 and uses the [esp32_can CAN Bus platform](https://esphome.io/components/canbus.html#esp32-can-component).

This is written and tested for the [Rixen's MCS7 hardware](https://rixens.com/collections/mcs-7-hydronic-system-documents). The CAN interface is pointed out on page 10 of the Rixen's [manual](https://cdn.shopify.com/s/files/1/0530/5362/0413/files/Rixen_s_Installation_Manual_-_NA_10.2023_-_Final.pdf?v=1697649451).

![Screenshot 2024-01-31 at 10 08 05 AM](https://github.com/mikegoubeaux/rixens-esphome/assets/9661510/394ea22f-41c4-4714-8a11-c7cb545bdce4)

![Screenshot 2023-11-06 at 1 32 22 PM](https://github.com/mikegoubeaux/rixens-esphome/assets/9661510/dfb0d1ca-18c2-4d9b-b036-19ced3874270)

## Pinouts

The CAN Bus pins are not labeled on the Rixens' control module. Here is a diagram of the pins. You can double check your pin out by metering the pins for 12v, ground, and CAN bus voltages. CAN Hi usually measures from 2.5V to 3.75V while CAN Lo measures from 2.5V to 1.25V.

<img width="562" alt="Rixens CAN bus pinout" src="https://github.com/mikegoubeaux/rixens-esphome/assets/9661510/9141288c-cbe0-469c-b7b9-9b02a6126366">
