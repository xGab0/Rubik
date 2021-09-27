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
      "pregame",
      "game",
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
      "watchers:blue",
      "watchers:green",
      "watchers:red",
      "watchers:yellow",
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
  "states": [
    "waiting",
    "starting",
    "pregame",
    "game",
    "end"
  ],
  "default_state": "waiting"
}
```
