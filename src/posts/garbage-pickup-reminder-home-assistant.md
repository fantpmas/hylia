---
title: 'Garbage pickup reminder via Home Assistant'
socialImage: https://www.fantomas-ls.com/images/recycle.jpg
date: '2021-06-18'
tags:
  - tech
  - home-assistant
---

Using afvalbeheer's `recycleapp_morgen` sensor, you can easily send a notification to your phone the day before garbage pickup.​


1. Install the custom component [afvalbeheer](https://github.com/pippyn/Home-Assistant-Sensor-Afvalbeheer).
2. Configure your waste collector in `/config/configuration.yaml`, and make sure to add `upcomingsensor: 1`. I use `RecycleApp` for Belgium.

```yaml
sensor:
 - platform: afvalbeheer
   wastecollector: RecycleApp
   resources:
    - restafval
    - papier
    - pmd
   postcode: 9000
   streetnumber: 666
   streetname: Duivelsteeg
   upcomingsensor: 1
   builtinicons: 1
```

3. Add the following config to `/config/automations.yaml`.
{% raw %}
```yaml

  - alias: 'Send Garbage Reminder'
    trigger:
    - platform: state
      entity_id:
        - sensor.recycleapp_morgen
    condition:
      condition: time
      weekday:
        - mon
    action:
      - service: notify.mobile_app_iPhone
        data:
          message: "♻️ Morgen: {{ states.sensor.recycleapp_morgen.state }}"
```
{% endraw %}

By using [platform: state](https://www.home-assistant.io/docs/automation/trigger/#state-trigger) the automation is triggered when the state of `sensor.recycleapp_morgen` changes. This happens when it is the day before pickup and then returns the items that are being collected.

Pickup day is Tuesday so I added a time condition to show the notification on Monday.

Then simply add an action to notify your mobile phone and presto!

![Garbage collection reminder](/images/recycle.jpg "No more excuses!")



