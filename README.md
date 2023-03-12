# Example Data Templates

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
<summary>Template</summary>
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
</p>
</details>

<details>
<summary>Example</summary>
<p>

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
| might | object | The model's might stats |
| will | object | The model's will stats |
| fate | object | The model's fate stats |

### Might, Will & Fate Objects

| Property | Type | Description |
| --- | --- | --- |
| additional | number | The additional amount of might points that can be bought for a model e.g. Ringwriath, Witch-King |
| points | number | The cost in points of the additional stat per point e.g. 5 points. 0 if model can't have additional points. |
| value | number | The model's un-modified default stat value |

</p></details>

<details>
<summary>Template</summary>
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
            "additional": 0,
            "points": 0,
            "value": 0
        },
        "will": {
            "additional": 0,
            "points": 0,
            "value": 0
        },
        "fate": {
            "additional": 0,
            "points": 0,
            "value": 0
        }
    }
```

</p>
</details>

<details>
<summary>Example</summary>
<p>

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
            "additional": 3,
            "points": 5,
            "value": 0
        },
        "will": {
            "additional": 10,
            "points": 5,
            "value": 10
        },
        "fate": {
            "additional": 3,
            "points": 5,
            "value": 0
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
<summary>Template</summary>
<p>

```JSON5
"type": {
        "Type Of Model": {}
}
```
</p>
</details>

<details>
<summary>Example</summary>
<p>

```JSON5
"type": {
        "Monster": {},
        "Infantry": {}
        ... // Additonal Types

}
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

<details><summary>Template</summary>
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
            "type": "Default",
            "userSelected": false
        }
}
```
</p>
</details>

<details><summary>Example</summary>
<p>

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



