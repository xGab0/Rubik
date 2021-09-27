# Rubik
This is an example of a Rubik config designed for a 4x4x4x4 Bedwars game.

## 📜 Main json config
Here we have the overview of the config with all informations.
```json
{
  "states": {
    "list": [
      "waiting",
      "starting",
      "game",
      "dragons",
      "end"
    ],
    "default_state": "waiting"
  },
  "theater": {
    "watchers": [
      "blue",
      "green",
      "red",
      "yellow"
    ],
    "actors": [
      "blue",
      "green",
      "red",
      "yellow"
    ]
  },
  "vox": {
    "channels": [
      "teamchat:blue",
      "teamchat:green",
      "teamchat:red",
      "teamchat:yellow",
      "watchers:globalchat",
      "actors:globalchat"
    ],
    "groups": [
      "teamchat:blue",
      "teamchat:green",
      "teamchat:red",
      "teamchat:yellow"
    ]
  },
  "persona": {
    "groups": [
      "watchers:staff",
      "watchers:blue",
      "watchers:green",
      "watchers:red",
      "watchers:yellow",
      "actors:waiting"
      "actors:blue",
      "actors:green",
      "actors:red",
      "actors:yellow"
    ]
  },
  "stele": {
    "actionbars": [
      "watchers",
      "actors"
    ],
    "bossbars": [
      "watchers",
      "actors"
    ],
    "sidebars": [
      "watchers",
      "actors"
    ]
  }
}
```

### 📜 State json config
```json
{
  "name": "WAITING",
  "conditions": {
    "online": {
      "enabled": true,
      "value": 16,
      "state": "STARTING"
    },
    "duration": {
      "enabled": false,
      "value": -1,
      "state": "WAITING"
    }
  },
}
```
```json
{
  "name": "STARTING",
  "conditions": {
    "online": {
      "enabled": true,
      "value": 15,
      "state": "WAITING"
    },
    "duration": {
      "enabled": true,
      "value": 20,
      "state": "GAME"
    }
  },
}
```
```json
{
  "name": "GAME",
  "conditions": {
    "online": {
      "enabled": true,
      "value": 1,
      "state": "WAITING"
    },
    "duration": {
      "enabled": true,
      "value": 36000,
      "state": "DRAGONS"
    }
  },
}
```
```json
{
  "name": "DRAGONS",
  "conditions": {
    "online": {
      "enabled": true,
      "value": 1,
      "state": "WAITING"
    },
    "duration": {
      "enabled": false,
      "value": -1,
      "state": "WAITING"
    }
  },
}
```
```json
{
  "name": "END",
  "conditions": {
    "online": {
      "enabled": true,
      "value": 1,
      "state": "WAITING"
    },
    "duration": {
      "enabled": true,
      "value": 20,
      "state": "WAITING"
    }
  },
}
```

### 📜 Persona json config
persona/groups/en.json
```json
[
  {
    "name": "watchers:staff",
    "skin": "",
    "chat": "<bold><gray>staff<gradient></bold><white> %player% <dark_gray>➠ <white>%message%",
    "tag": {
      "interval": 7,
      "frames": [
          "<bold><gray>STAFF</gray></bold> <white>%player%"
      ]
    }
  },
  {
    "name": "watchers:blue",
    "skin": "",
    "chat": "<bold><blue>blue<gradient></bold><aqua> %player% <dark_gray>➠ <aqua>%message%",
    "tag": {
      "interval": 7,
      "frames": [
          "<bold><blue>BLUE</blue></bold> <aqua>%player%"
      ]
    }
  },
  {
    "name": "watchers:green",
    "skin": "",
    "chat": "<bold><dark_green>green<gradient></bold><green> %player% <dark_gray>➠ <green>%message%",
    "tag": {
      "interval": 7,
      "frames": [
          "<bold><dark_green>GREEN</dark_green></bold> <green>%player%"
      ]
    }
  },
  {
    "name": "watchers:red",
    "skin": "",
    "chat": "<bold><dark_red>red<gradient></bold><red> %player% <dark_gray>➠ <red>%message%",
    "tag": {
      "interval": 7,
      "frames": [
          "<bold><dark_red>RED</red></bold> <red>%player%"
      ]
    }
  },
  {
    "name": "watchers:yellow",
    "skin": "",
    "chat": "<bold><gold>yellow<gradient></bold><yellow> %player% <dark_gray>➠ <yellow>%message%",
    "tag": {
      "interval": 7,
      "frames": [
          "<bold><gold>YELLOW</red></bold> <yellow>%player%"
      ]
    }
  },
  {
    "name": "actors:waiting",
    "skin": "",
    "chat": "<bold><gray>user<gradient></bold><white> %player% <dark_gray>➠ <white>%message%",
    "tag": {
      "interval": 7,
      "frames": [
          "<bold><gray>USER</gray></bold> <white>%player%"
      ]
    }
  },
  {
    "name": "actors:blue",
    "skin": "",
    "chat": "<bold><blue>blue<gradient></bold><aqua> %player% <dark_gray>➠ <aqua>%message%",
    "tag": {
      "interval": 7,
      "frames": [
          "<bold><blue>BLUE</blue></bold> <aqua>%player%"
      ]
    }
  },
  {
    "name": "actors:green",
    "skin": "",
    "chat": "<bold><dark_green>green<gradient></bold><green> %player% <dark_gray>➠ <green>%message%",
    "tag": {
      "interval": 7,
      "frames": [
          "<bold><dark_green>GREEN</dark_green></bold> <green>%player%"
      ]
    }
  },
  {
    "name": "actors:red",
    "skin": "",
    "chat": "<bold><dark_red>red<gradient></bold><red> %player% <dark_gray>➠ <red>%message%",
    "tag": {
      "interval": 7,
      "frames": [
          "<bold><dark_red>RED</red></bold> <red>%player%"
      ]
    }
  },
  {
    "name": "actors:yellow",
    "skin": "",
    "chat": "<bold><gold>yellow<gradient></bold><yellow> %player% <dark_gray>➠ <yellow>%message%",
    "tag": {
      "interval": 7,
      "frames": [
          "<bold><gold>YELLOW</red></bold> <yellow>%player%"
      ]
    }
  }
]
```
persona/groups/it.json
```json
[
  {
    "name": "watchers:staff",
    "skin": "",
    "chat": "<bold><gray>staff<gradient></bold><white> %player% <dark_gray>➠ <white>%message%",
    "tag": {
      "interval": 7,
      "frames": [
          "<bold><gray>STAFF</gray></bold> <white>%player%"
      ]
    }
  },
  {
    "name": "watchers:blue",
    "skin": "",
    "chat": "<bold><blue>blu<gradient></bold><aqua> %player% <dark_gray>➠ <aqua>%message%",
    "tag": {
      "interval": 7,
      "frames": [
          "<bold><blue>BLU</blue></bold> <aqua>%player%"
      ]
    }
  },
  {
    "name": "watchers:green",
    "skin": "",
    "chat": "<bold><dark_green>verde<gradient></bold><green> %player% <dark_gray>➠ <green>%message%",
    "tag": {
      "interval": 7,
      "frames": [
          "<bold><dark_green>VERDE</dark_green></bold> <green>%player%"
      ]
    }
  },
  {
    "name": "watchers:red",
    "skin": "",
    "chat": "<bold><dark_red>rosso<gradient></bold><red> %player% <dark_gray>➠ <red>%message%",
    "tag": {
      "interval": 7,
      "frames": [
          "<bold><dark_red>ROSSO</red></bold> <red>%player%"
      ]
    }
  },
  {
    "name": "watchers:yellow",
    "skin": "",
    "chat": "<bold><gold>giallo<gradient></bold><yellow> %player% <dark_gray>➠ <yellow>%message%",
    "tag": {
      "interval": 7,
      "frames": [
          "<bold><gold>GIALLO</red></bold> <yellow>%player%"
      ]
    }
  },
  {
    "name": "actors:waiting",
    "skin": "",
    "chat": "<bold><gray>utente<gradient></bold><white> %player% <dark_gray>➠ <white>%message%",
    "tag": {
      "interval": 7,
      "frames": [
          "<bold><gray>UTENTE</gray></bold> <white>%player%"
      ]
    }
  },
  {
    "name": "actors:blue",
    "skin": "",
    "chat": "<bold><blue>blu<gradient></bold><aqua> %player% <dark_gray>➠ <aqua>%message%",
    "tag": {
      "interval": 7,
      "frames": [
          "<bold><blue>BLU</blue></bold> <aqua>%player%"
      ]
    }
  },
  {
    "name": "actors:green",
    "skin": "",
    "chat": "<bold><dark_green>verde<gradient></bold><green> %player% <dark_gray>➠ <green>%message%",
    "tag": {
      "interval": 7,
      "frames": [
          "<bold><dark_green>VERDE</dark_green></bold> <green>%player%"
      ]
    }
  },
  {
    "name": "actors:red",
    "skin": "",
    "chat": "<bold><dark_red>rosso<gradient></bold><red> %player% <dark_gray>➠ <red>%message%",
    "tag": {
      "interval": 7,
      "frames": [
          "<bold><dark_red>ROSSO</red></bold> <red>%player%"
      ]
    }
  },
  {
    "name": "actors:yellow",
    "skin": "",
    "chat": "<bold><gold>giallo<gradient></bold><yellow> %player% <dark_gray>➠ <yellow>%message%",
    "tag": {
      "interval": 7,
      "frames": [
          "<bold><gold>GIALLO</red></bold> <yellow>%player%"
      ]
    }
  }
]
```
