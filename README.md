# My "Dark Thermostat" Config

My custom multi-card configuration using Dark Thermostat card for my Nest Thermostat

![image](https://user-images.githubusercontent.com/49846893/202269236-fb192ab6-2408-492f-ad70-48f9a14e6023.png)

![image](https://user-images.githubusercontent.com/49846893/202269558-de8d2062-2676-4dad-8a66-4575ff07a4b2.png)

Addional components required:
 - [browser-mod](https://github.com/thomasloven/hass-browser_mod)
 - [card-mod](https://github.com/thomasloven/lovelace-card-mod)
 - [custom:button-card](https://github.com/custom-cards/button-card)
 - [custom:popup-card](https://github.com/thomasloven/lovelace-popup-card)
 - [custom:scheduler-card](https://github.com/nielsfaber/scheduler-card)
 - [custom:thermostat-dark-card](https://github.com/ciotlosm/lovelace-thermostat-dark-card)
 - [custom:vertical-stack-in-card](https://github.com/ofekashery/vertical-stack-in-card)
 - [HACS Scheduler Component](https://github.com/nielsfaber/scheduler-component)
 
Thermostat: climate.living_room (from Nest Integration)

Custom sensors:
 - nest_eco_high
 - nest_eco_low
 - nest_eco_temp
 - nest_heating_runtime
 - nest_humidity
 - nest_hvac_action
 - nest_preset_mode
 - nest_room_hvac_mode
 - nest_setpoint
 - nest_temperature
 - sensor.nest_time_to_temp_message
 - sensor.outside_weather_temperature

Copy the code from lovelace_raw_config.yaml and add it as a new view in your ui.lovelace.yaml or your lovelace dashboard raw configuration

Helpers:

![image](https://user-images.githubusercontent.com/49846893/202268919-3b7732e2-8e0d-44cd-8555-1d7e26fd7113.png)![image](https://user-images.githubusercontent.com/49846893/202268689-f87263f5-38fc-4782-84c4-d6e08dbfe773.png)

sensors.yaml is formatted for the template integration using the modern configuration for variable names.

See [Modern Configuration Variables](https://www.home-assistant.io/integrations/template/#configuration-variables/)

Sample configuration.yaml entry:
```
template:
  - sensor:
    - name: "Nest Heating Runtime"
      unique_id: nest_heat_runtime
      unit_of_measurement: 'seconds'
      state: "{{state_attr('climate.living_room','elapsed_seconds')|float(0) }}"
      ...
```

To use legacy format templating, somewhat extensive changes are required for variable names and formatting.

See [Legacy Configuration Variables](https://www.home-assistant.io/integrations/template/#configuration-variables/)

i.e. the above code would become:
```
sensor:
  - platform: template
    sensors:
      nest_heating_runtime:
        friendly_name: Nest Heating Runtime
        unit_of_measurement: 'seconds'
        value_template:: "{{state_attr('climate.living_room','elapsed_seconds')|float(0) }}"
      ...
```
