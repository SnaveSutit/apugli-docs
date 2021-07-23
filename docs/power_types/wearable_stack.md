---
title: Wearable Stack (Power Type)
date: 2021-07-22
---

# Wearable Stack

[Power Type](../power_types.md).

A power that renders an item on the entity's head.

This only works on entities that can normally wear the specified item on their head (for example helmets work with zombies but wouldn't work with villagers but glass works with both of these mobs).

Only one of these powers will show up at a time.

Type ID: `apugli:wearable_stack`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`stack` | [Item Stack](https://origins.readthedocs.io/en/latest/data_types/item_stack/#item-stack) |  | The item stack to render on the entity's head.

### Example
```json
{
  "type": "apugli:wearable_stack",
  "stack": {
    "item": "minecraft:brown_carpet",
    "tag": "{CustomModelData:1}"
  },
  "scale": 1.5
}
```
This example would render brown carpet with a CustomModelData of 1 at 1.5 scale on the entity's head.