---
title: Rocket Jump (Power Type)
date: 2021-08-19
---

# Rocket Jump

[Power Type](../power_types.md).

An active power that launches the player through the air while leaving an explosion at their crosshair location.

Type ID: `apugli:rocket_jump`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`cooldown` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) |  | The number of ticks the player has to wait between uses of this power.
`hud_render` | [Hud Render](https://origins.readthedocs.io/en/latest/types/data_types/hud_render/) |  | Specifies how and if a cooldown bar is rendered.
`source` | [Damage Source](https://origins.readthedocs.io/en/latest/types/data_types/damage_source/) | *optional* | If set, this is the damage source that will be used to deal damage to the entity upon using this ability.
`amount` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | *optional*| How much damage will be dealt upon using this ability.
`speed` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | *optional* | The speed applied to the player in the opposite direction they are facing.
`use_charged` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Whether this ability should consume the TooManyOrigins' or CursedOrigins' Charged status effect for a more powerful blast. This has no effect unless either mod is initialized.
`key` | [Key](https://origins.readthedocs.io/en/latest/types/data_types/key/) | | Which active key this power should respond to.


### Example
```json
{
  "type": "apugli:rocket_jump",
  "cooldown": 5,
  "hud_render": {
    "should_render": true,
    "sprite_location": "toomanyorigins:textures/gui/tmo_resource_bar.png",
    "bar_index": 2
  },
  "source": {
    "name": "overheat",
    "bypasses_armor": "true",
    "fire": "true",
    "unblockable": "true"
  },
  "key": {
    "key": "key.origins.primary_active",
    "continuous": false
  },
  "amount": 2.0,
  "should_use_charged": true,
  "speed": 1.0
}
```
This power allows a player to launch themself through the air while taking 1 heart of armor bypassing, unblockable fire damage named overheat. This ability considers the Charged status effect from TooManyOrigins and CursedOrigins.