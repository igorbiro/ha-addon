# Source Code Link

-   [FrontEnd](https://github.com/CoolKit-Technologies/ha-addon-frontEnd)
-   [BackEnd](https://github.com/CoolKit-Technologies/ha-addon-backEnd)

# Home-Assistant-AddOn

## ADD-ON:

-   Refer to [Wiki](https://bit.ly/eWeLinkaddon)

## DOCKER:

-   **Use host network to discover and control DIY and LAN devices.**
-   **Currently, port forwarding is not supported, please make sure that port 3000 is idle.**

1. `git clone https://github.com/CoolKit-Technologies/ha-addon.git`
2. `cd ha-addon/eWeLink_Smart_Home/`
3. `docker build . -t ewelink_smart_home`
4. Run the code below. Replace `yourHomeAssistantUrl` with your current Home Assisant URL.

```
docker run -d \
    --restart=always \
    --network host \
    -e HA_URL=yourHomeAssistantUrl \
    ewelink_smart_home
```

-   Example:

```
  docker run -d \
  --restart=always \
  --network host \
  -e HA_URL=http://192.168.1.100:8123 \
  ewelink_smart_home
```

5. Access port `4000`.
