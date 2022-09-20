# Home Assistant Real-Time Sports Score Card
A Home Assistant frontend custom card that will display real-time updates for teams tracked with the [ha-teamtracker](https://github.com/vasqued2/ha-teamtracker) integration by @vasqued2.  Has custom in-game layouts for football, baseball, basketball, and soccer.

This card was strongly based on the fantastic [ha-nfl-card](https://github.com/D34DC3N73R/ha-nfl-card) by @D34DC3N73R.

#### Version Compatibility
 - Releases for [ha-teamtracker](https://github.com/vasqued2/ha-teamtracker) and [ha-teamtracker-card](https://github.com/vasqued2/ha-teamtracker-card) will follow the MAJOR.MINOR.PATCH convention.
 - All teamtracker and teamtracker-card releases with the same MAJOR and MINOR version numbers will be compatible, regardless of PATCH version.
 - For example, any teamtracker v0.2.x will be compatible with any teamtracker-card v0.2.y.
 - Compatibility is not guaranteed across MAJOR or MINOR version numbers.

### &nbsp;&nbsp;&nbsp;PRE Game Examples

<img width="409" alt="PRE-football" src="https://user-images.githubusercontent.com/17114183/187316418-86927b91-d4cb-4d6d-9125-13045a1b6c9a.png">
<img width="410" alt="PRE-hockey" src="https://user-images.githubusercontent.com/17114183/187316485-68bd6d2a-2784-4c4c-8793-045b83335cef.png">
<img width="409" alt="PRE-basketball" src="https://user-images.githubusercontent.com/17114183/187316566-27edc6c2-b68d-4b12-ae58-a56bb6a4db59.png">

### &nbsp;&nbsp;&nbsp;IN Game Examples

![IN-baseball](https://user-images.githubusercontent.com/17114183/187316734-53688f9c-bd7a-44a1-b3a6-36894c5669c2.png)
<img width="409" alt="IN-soccer" src="https://user-images.githubusercontent.com/17114183/187316787-97aca588-56c3-4737-9df6-aef86fc0c503.png">
![IN-football](https://user-images.githubusercontent.com/17114183/187316807-b694d4ad-a895-4047-a700-264b41f91adc.png)

### &nbsp;&nbsp;&nbsp;POST Game Examples

![POST-football](https://user-images.githubusercontent.com/17114183/187316885-7bbff2de-0382-47be-b775-116a45b9b636.png)
![POST-soccer2](https://user-images.githubusercontent.com/17114183/187316901-d40f8e2f-b86d-4cab-9713-976402cd94fb.png)

### &nbsp;&nbsp;&nbsp;BYE and NOT FOUND (No Upcoming Game) Examples

![NF-hockey](https://user-images.githubusercontent.com/17114183/187316958-617173d1-a6f2-4cf5-8abe-3a58ae40ff8e.png)
![NF-ncaaf](https://user-images.githubusercontent.com/17114183/187316966-495ca610-c28a-401d-a4a1-080445d98894.png)
![NF-football](https://user-images.githubusercontent.com/17114183/187316983-998527e7-c75d-421a-8833-d00e7ddb4ddc.png)

## HACS Installation
 - In the HACS UI, click the 3 dots in the upper right
 - Click 'Add Custom Repository'
 - Fill in the repo url https://github.com/vasqued2/ha-teamtracker-card and choose 'Lovelace' category.
 - install the custom card
 - Add the following to your resources
```
url: /hacsfiles/ha-teamtracker-card/ha-teamtracker-card.js
type: Javascript Module
```

## Manual Installation
 - Download [ha-teamtracker-card.js](https://github.com/vasqued2/ha-teamtracker-card/blob/main/dist/ha-teamtracker-card.js)
 - Copy to www/community/ha-teamtracker-card/ (make the ha-teamtracker-card directory first)
 - Add the following to your resources
```
url: /hacsfiles/ha-teamtracker-card/ha-teamtracker-card.js
type: Javascript Module
```

## Options
| Name | Description | Default | Required |  Values |
| --- | --- | --- | --- | --- |
| `entity` | Name of ha-teamtracker sensor | `sensor.team_tracker` | Yes  | Valid sensor |
| `outline` | Outline team colors (helpful w/ dark themes) |`false` | No |  `true` `false` |
| `outline_color` | Specifies outline color. | `white` | No |  CSS color or hex value  |

## Examples
```
type: 'custom:teamtracker-card'
entity: sensor.team_tracker
outline: true
outline_color: deeppink
```

![PINK-example](https://user-images.githubusercontent.com/17114183/187317324-f1a9764b-5443-46e5-b000-b9c61a7856ef.png)

```
type: 'custom:teamtracker-card'
entity: sensor.team_tracker
outline: true
outline_color: '#ffe500'
```

![OUTLINE-example](https://user-images.githubusercontent.com/17114183/187317354-496ed84a-fe27-496d-a75e-7163fcea3845.png)


## Minimal Required Configuration
```
type: 'custom:teamtracker-card'
entity: sensor.team_tracker
```
Where `sensor.team_tracker` is the sensor name from the [ha-teamtracker](https://github.com/vasqued2/ha-teamtracker) integration.
