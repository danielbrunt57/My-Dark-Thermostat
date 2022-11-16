# My "Dark Thermostat" Config

My custom multi-card configuration using Dark Thermostat card for my Nest Thermostat

![image](https://user-images.githubusercontent.com/49846893/202269236-fb192ab6-2408-492f-ad70-48f9a14e6023.png)

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
 - nest_eco_low
 - nest_eco_high
 - living_room_eco_temp
 - living_room_hvac_action
 - living_room_hvac_mode
 - living_room_preset_mode
 - living_room_setpoint
 - living_room_temperature
 - sensor.nest_time_to_temp_message
 - sensor.outside_weather_temperature

Copy the code from lovelace_raw_config.yaml and add it as a new view in your ui.lovelace.yaml or your lovelace dashboard raw configuration

Helpers:

![image](https://user-images.githubusercontent.com/49846893/202268919-3b7732e2-8e0d-44cd-8555-1d7e26fd7113.png)![image](https://user-images.githubusercontent.com/49846893/202268689-f87263f5-38fc-4782-84c4-d6e08dbfe773.png)
