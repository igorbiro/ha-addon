# eWeLink Smart Home

---

## Troubleshooting

-   To solve `Failed to call service switch/turn_on. Service not found.` issue, use`File editor` to edit `configuration.yaml`. Append the following info to end of file:

```
switch:
  - platform: template
    switches:
      ewelink_virtual_switch:
        turn_on:
          service: switch.turn_on
        turn_off:
          service: switch.turn_off

```

---

-   To solve `Failed to call service cover.open_cover. Service not found.` issue, use`File editor` to edit `configuration.yaml`. Append the following info to end of file:

```
cover:
  - platform: template
    covers:
      ewelink_create_cover_service:
        open_cover:
          service: cover.open_cover
        close_cover:
          service: cover.close_cover
        stop_cover:
          service: cover.stop_cover
        set_cover_position:
          service: cover.set_cover_position
```
