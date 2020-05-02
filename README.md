# BMW Connected Drive Custom Component for Development
Home Assistant Custom Component of BMW Connected Drive **for development purposes only**!
For details please see [the official component documentation](https://www.home-assistant.io/integrations/bmw_connected_drive/) or [the bimmer_connected library](https://github.com/bimmerconnected/bimmer_connected).

### Installation (HACS)
When using HACS, just add this repository as a [custom repostiory](https://hacs.xyz/docs/navigation/settings#custom-repositories) of category `Integration` with the url `https://github.com/bimmerconnected/ha_custom_component`.

### Installation (manual)
Place the folder `bmw_connected_drive` and all it's files in the folder `custom_components` in the config folder of HA (where configuration.yaml is).

# Release notes
## 20200502.1 - Notifications via `notify`, new API backend
With this version you can use the following new options using the new notify component:
* Send notifications to your car
* Send Point of Interest (POI) to your car

You can test this by using Developer Tools - Services and select `notify.bmw_connected_drive_<car>`

For a message use these service data:
```
title: Your title here (if left empty it will be Home Assistant)
message: Your message here
```

For a POI:
```
message: The name of the location (this is shown on the iDrive dashboard)
data:
  location:
    latitude: 48.177024
    longitude: 11.559107
    street: Street name  # Optional
    city: City name  # Optional
    postal_code: Postal Code  # Optional
    country: Country  # Optional
```

#### Pictures
Here are some pictures, not too sharp and yeah it's a touch screen, but they give a good impression

Overview of messages
![Example 1](/pictures/example_1.jpg)

Example of message
![Example 2](/pictures/example_2.jpg)

Example of POI
![Example 3](/pictures/example_3.jpg)
