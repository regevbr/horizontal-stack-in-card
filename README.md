# Horizontal Stack In Card

![Version](https://img.shields.io/github/v/release/regevbr/horizontal-stack-in-card)
![Downloads](https://img.shields.io/github/downloads/regevbr/horizontal-stack-in-card/total)
![Version](https://img.shields.io/github/v/release/regevbr/horizontal-stack-in-card)
![Stars](https://img.shields.io/github/stars/regevbr/horizontal-stack-in-card)

Horizontal Stack In Card allows you to group multiple cards in one card.

#### Please ⭐️ this repo if you find it useful

![Example](https://user-images.githubusercontent.com/16443111/80155963-779f3800-85cb-11ea-9565-c360eb9dffb1.png)

## Options

| Name       | Type    | Default      | Description                               |
| ---------- | ------- | ------------ | ----------------------------------------- |
| type       | string  | **Required** | `custom:horizontal-stack-in-card`           |
| cards      | list    | **Required** | List of cards                             |
| title      | string  | **Optional** | Card title                                |
| horizontal | boolean | **Optional** | Default: `false`                          |
| styles     | object  | **Optional** | Adds custom CSS directives to child cards |

## Installation

1. Install the `horizontal-stack-in-card` card by copying `horizontal-stack-in-card.js` to `<config directory>/www/horizontal-stack-in-card.js`

Bash:

```bash
wget https://raw.githubusercontent.com/regevbr/horizontal-stack-in-card/master/horizontal-stack-in-card.js
mv horizontal-stack-in-card.js /config/www/
```

2. Link `horizontal-stack-in-card` inside your `ui-lovelace.yaml`

```yaml
resources:
  - url: /local/horizontal-stack-in-card.js?v=0.4.1
    type: js
```

3. Add a custom card in your `ui-lovelace.yaml`

**Example**

```yaml
type: 'custom:horizontal-stack-in-card'
title: My Card
cards:
  - type: glance
    entities:
      - sensor.temperature_sensor
      - sensor.humidity_sensor
      - sensor.motion_sensor
  - type: entities
    entities:
      - switch.livingroom_tv
      - entity: script.livingroom_receiver
        name: Receiver
      - switch.livingroom_ac
```

## Credits

- [regevbr](https://github.com/regevbr)
- [ofekashery](https://github.com/ofekashery)
- [ciotlosm](https://github.com/ciotlosm)
- [thomasloven](https://github.com/thomasloven)
