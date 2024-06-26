# Model Profile Templates & Examples

## Model Profile
<details>
<summary>Template</summary>
<p>

```JSON5
{
    "actions": {
        "Name Of Action": {},
        "Name Of Action": {}
    },
    "armies": {
        "Army Name": {
            "tier": "",
            "selectableInWarband": true,
            "warbandSize": 0
        },
        "Army Name": {
            "tier": "",
            "selectableInWarband": true,
            "warbandSize": 0
        },
        "Army Name": {
            "tier": "",
            "selectableInWarband": true,
            "warbandSize": 0
        }
    },
    "magic": {
        "Name Of Magic Power": {
            "casting": 0,
            "range": 0
        },
        "Name Of Magic Power": {
            "casting": 0,
            "range": 0
        },
        "Name Of Magic Power": {
            "casting": 0,
            "range": 0
        }
    },
    "modelCount": 1,
    "mounts": {
        "Name Of Mount": {
            "points": 0,
            "userSelected": false
        },
        "Name Of Mount": {
            "points": 0,
            "userSelected": false
        },
        "Name Of Mount": {
            "points": 0,
            "userSelected": false
        }
    },
    "name": "",
    "points": 0,
    "race": {
        "Name Of Race": {},
        "Name Of Race": {}
    },
    "rules": {
        "Name Of Rule": {
            "type": "Passive"
        },
        "Name Of Rule": {
            "type": "Active"
        },
        "Name Of Rule": {
            "type": "Brutal Power Attack"
        }
    },
    "stats": {
        "movement": 0,
        "fight": 0,
        "range": 0,
        "strength": 0,
        "defence": 0,
        "attacks": 0,
        "wounds": 0,
        "courage": 0,
        "might": {
            "min": 0,
            "max": 0,
            "points": 0,
            "current": 0,
            "asterisk": null
        },
        "will": {
            "min": 0,
            "max": 0,
            "points": 0,
            "current": 0,
            "asterisk": null
        },
        "fate": {
            "min": 0,
            "max": 0,
            "points": 0,
            "current": 0,
            "asterisk": null
        }
    },
    "type": {
        "Monster": {},
        "Infantry": {}
    },
    "version": 0,
    "wargear": {
        "Wargear Name": {
            "optional": true,
            "points": 5,
            "type": "Active",
            "userSelected": false
        },
        "Wargear Name": {
            "optional": false,
            "points": 5,
            "type": "Passive",
            "userSelected": false
        }
    }
}
```

</p>
</details>

## Actions
<details>
<summary>Properties</summary>
<p>

| Property | Type | Description |
| --- | --- | --- |
| Name Of Action | string | The name of this model in Capital Case. |

</p>
</details>

<details>
<summary>Template & Example</summary>
<p>

```JSON5
    "actions": {
        "Name Of Action": {},
        "Name Of Action": {}
    }
```

```JSON5
    "actions": {
        "Channelling": {},
        "March": {}
    }
```

</p>
</details>


## Armies, Tiers & Warband Size
<details>
<summary>Properties</summary>
<p>

| Property | Type | Description |
| --- | --- | --- |
| Army Name | string | The name of the army this model belongs to in Capital Case. |
| tier | "Hero of Legend" \| "Hero of Valour" \| "Hero of Fortitude" \| "Minor Hero"\| "Independent Hero" \| "Warrior" | The tier of this model in the specified army in Capital Case. |
| warbandSize | number | The maximum warband size this model is allowed. 0 if this model isn't a hero. |
| selectableInWarband | boolean | Can this model be selected as part of another models warband (Default should be true). |

</p>
</details>

<details>
<summary>Template & Example</summary>
<p>

```JSON5
    "armies": {
        "Army Name": {
            "tier": "",
            "selectableInWarband": true,
            "warbandSize": 0
        },
        "Army Name": {
            "tier": "",
            "selectableInWarband": true,
            "warbandSize": 0
        },
        "Army Name": {
            "tier": "",
            "selectableInWarband": true,
            "warbandSize": 0
        }
    }
```

```JSON5
    "armies": {
        "Angmar": {
            "tier": "Hero of Legend",
            "selectableInWarband": true,
            "warbandSize": 18
        },
        "Barad-Dûr": {
            "tier": "Hero of Valour",
            "selectableInWarband": true,
            "warbandSize": 15
        },
        "Mordor": {
            "tier": "Hero of Legend",
            "selectableInWarband": true,
            "warbandSize": 18
        }
    }
```

</p>
</details>


## Magic
<details>
<summary>Properties</summary>
<p>

| Property | Type | Description |
| --- | --- | --- |
| Name Of Magic Power | string | The name of the Magical Power that this model has in Capital Case. |
| casting | number | The model's casting score for this Magical Power. |
| range | number | The distance in inches a model can cast the Magical Power. |    

</p>
</details>

<details>
<summary>Template & Example</summary>
<p>

```JSON5
    "magic": {
        "Name Of Magic Power": {
            "casting": 0,
            "range": 0
        },
        "Name Of Magic Power": {
            "casting": 0,
            "range": 0
        },
        "Name Of Magic Power": {
            "casting": 0,
            "range": 0
        }
    }
```

```JSON5
    "magic": {
        "Instill Fear": {
            "casting": 5,
            "range": 3
        },
        "Transfix": {
            "casting": 3,
            "range": 12
        },
        "Compel": {
            "casting": 4,
            "range": 12
        }
    }
```

</p>
</details>


## Model Count
<details>
<summary>Properties</summary>
<p>

| Property | Type | Description |
| --- | --- | --- |
| modelCount | number | The quantity of the model, should always be 1. |

</p>
</details>

<details>
<summary>Template & Example</summary>
<p>

```JSON5
    "modelCount": 1
```

</p>
</details>


## Mounts
<details>
<summary>Properties</summary>
<p>

| Property | Type | Description |
| --- | --- | --- |
| Name Of Mount | string | The name of the mount in Capital Case. |
| points | number | The cost in points of the mount. |
| userSelected | boolean | Default (false), changes when a user selects it (true).  |


</p>
</details>

<details>
<summary>Template & Example</summary>
<p>

```JSON5
    "mounts": {
        "Name Of Mount": {
            "points": 0,
            "userSelected": false
        },
        "Name Of Mount": {
            "points": 0,
            "userSelected": false
        },
        "Name Of Mount": {
            "points": 0,
            "userSelected": false
        }
        ... // Additonal Mounts
    }
```

```JSON5
    // Witch-King Mounts
    "mounts": {
        "Armoured Fell Beast": {
            "points": 70,
            "userSelected": false
        },
        "Armoured Horse": {
            "points": 15,
            "userSelected": false
        },
        "Fell Beast": {
            "points": 50,
            "userSelected": false
        },
        "Horse": {
            "points": 10,
            "userSelected": false
        }
    }
```

</p>
</details>


## Name
<details>
<summary>Properties</summary>
<p>

| Property | Type | Description |
| --- | --- | --- |
| name | string | The name of this model in Capital Case. |

</p>
</details>

<details>
<summary>Template & Example</summary>
<p>

```JSON5
    "uniqueName": ""
```

```JSON5
    "uniqueName": "The Witch-King Of Angmar"
```

</p>
</details>


## Points
<details>
<summary>Properties</summary>
<p>

| Property | Type | Description |
| --- | --- | --- |
| points | number | the base cost of this model. |

</p>
</details>

<details>
<summary>Template & Example</summary>
<p>

```JSON5
    "points": 0
```

```JSON5
    // Witch-King Base Cost
    "points": 70
```

</p>
</details>


## Race
<details>
<summary>Properties</summary>
<p>

| Property | Type | Description |
| --- | --- | --- |
| Name Of Race | string | The Race of this model in Capital Case. |

</p>
</details>

<details>
<summary>Template & Example</summary>
<p>

```JSON5
    "race": {
        "Name Of Race": {},
        "Name Of Race": {}
    }
```

```JSON5
    // With-King Race Details
    "race": {
        "Spirit": {},
        "Ringwraith": {}
    }
```

</p>
</details>


## Rules
<details>
<summary>Properties</summary>
<p>

| Property | Type |Description |
| --- | --- | --- |
| Name Of Rule | string | The name for rule of this model in Capital Case.  |
| type | "Active" \| "Brutal Power Attack" \| "Passive" | The classification of this Rule. |

</p>
</details>

<details>
<summary>Template & Example</summary>
<p>

```JSON5
"rules": {
        "Name Of Rule": {
            "type": "Passive"
        },
        "Name Of Rule": {
            "type": "Active"
        },
        "Name Of Rule": {
            "type": "Brutal Power Attack"
        }
    }
```

```JSON5
"rules": {
        // With-King Rules
        "Terror": {
            "type": "Passive"
        },
        "Will Of Evil": {
            "type": "Passive"
        },
        "Harbinger Of Evil": {
            "type": "Passive"
        }
    }
```
</p>
</details>


## Stats
<details>
<summary>Properties</summary>
<p>

| Property | Type | Description |
| --- | --- | --- |
| movement | number | The number in inches a model can move. |
| fight | number | The model's fight score. |
| range | number | The model's ranged fight score
| strength | number | The model's strength score. |
| defence | number | The model's defence score. |
| attacks | number | The number of attacks the model can make in melee combat. |
| wounds | number | The model's wounds score. |
| courage | number | The model's courage score. |
| might , will & fate | object | The model's Might, Will & Fate stats |
| min | number | The lowest amount of might points that can be bought for a model e.g. Ringwriath, Witch-King |
| max | number | The highest amount of might points that can be bought for a model e.g. Ringwriath, Witch-King |
| points | number | The cost in points of the additional stat per point e.g. 5 points. 0 if model can't have additional points. |
| current | number | The model's un-modified default stat value |
| asterisk | string | The * or ** if denoted in the profile e.g. The Dark Lord Sauron |

</p></details>

<details>
<summary>Template & Example</summary>
<p>

```JSON5
"stats": {
        "movement": 0,
        "fight": 0,
        "range": 0,
        "strength": 0,
        "defence": 0,
        "attacks": 0,
        "wounds": 0,
        "courage": 0,
        "might": {
            "min": 0,
            "max": 0,
            "points": 0,
            "current": 0,
            "asterisk": null
        },
        "will": {
            "min": 0,
            "max": 0,
            "points": 0,
            "current": 0,
            "asterisk": null
        },
        "fate": {
            "min": 0,
            "max": 0,
            "points": 0,
            "current": 0,
            "asterisk": null
        }
    }
```

```JSON5
"stats": {
        // Witch-King Stats
        "movement": 6,
        "fight": 5,
        "range": 4,
        "strength": 4,
        "defence": 8,
        "attacks": 1,
        "wounds": 1,
        "courage": 6,
        "might": {
            "min": 0,
            "max": 3,
            "points": 5,
            "current": 0,
            "asterisk": null
        },
        "will": {
            "min": 10,
            "max": 20,
            "points": 5,
            "current": 10,
            "asterisk": null
        },
        "fate": {
            "min": 0,
            "max": 3,
            "points": 5,
            "current": 0,
            "asterisk": null
        }
    }
```
</p>
</details>


## Type
<details>
<summary>Properties</summary>
<p>


| Property | Type |Description |
| --- | --- | --- |
| Type Of Model | "Cavalry" \| "Infantry" \| "Monster" | The types for this model.  |

</p>
</details>

<details>
<summary>Template & Example</summary>
<p>

```JSON5
"type": {
        "Type Of Model": {}
}
```

```JSON5
"type": {
        "Monster": {},
        "Infantry": {}
        ... // Additonal Types

}
```
</p>
</details>


## Version
<details><summary>Properties</summary>
<p>

| Property | Type | Description |
| --- | --- | --- |
| version | number | The semantic versioning of this JSON file. |

</p>
</details>

<details>
<summary>Template & Example</summary>
<p>

```JSON5
    "version": 0
```

```JSON5
"version": 1.0
```
</p>
</details>


## Wargear
<details><summary>Properties</summary>
<p>

| Property | Type | Description |
| --- | --- | --- |
| Wargear Name | string | The name of the wargear in Capital Case format. |
| optional | boolean | Should this wargear be selectable by the user (true), or is it part of default wargear for the model (false). |
| points | number | The cost in points of the wargear. 0 if wargear is part of default wargear for the model |
| type | "Active" \| "Passive" | Is this wargear passive or active in its use. |
| userSelected | boolean | Default (false), changes when a user selects it (true).  |
</p>
</details>

<details>
<summary>Template & Example</summary>
<p>

```JSON5
"wargear": {
        // Selectable Wargear
        "Wargear Name": {
            "optional": true,
            "points": 5, 
            "type": "Active",
            "userSelected": false
        },
        // Default Wargear
        "Wargear Name": {
            "optional": false,
            "points": 5, 
            "type": "Passive",
            "userSelected": false
        }
}
```

```JSON5
"wargear": {
        "Crown Of Morgul": {
            "optional": true,
            "points": 25,
            "type": "Passive",
            "userSelected": false
        },
        ... // Additonal Wargear
}
```
</p>
</details>
