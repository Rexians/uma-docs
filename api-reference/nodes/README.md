---
description: Gets nodes we currently have data for
---

# /nodes



{% swagger method="get" path="/nodes" baseUrl="https://api.rexians.tk" summary="Gets list of nodes" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="Successful response for all nodes" %}
```javascript
{
    "data": {
        "1": {
            "node_name": "A Good Defense",
            "node_info": "The Attacker's Well-Timed Blocks place a random Debuff from Weakness, Armor Break, Suppression, or Disorient on the Defender for 13 second(s). Each time the Attacker Dodges an Attack, place a random Buff from Fury, Armor Up, Power Gain, or Precision on the Attacker for 13 second(s)."
        },
        "2": {
            "node_name": "Academic Constitution",
            "node_info": "Science Attackers reduce the potency of the Defender's Poison effects by 85%. Additionally, whenever a Science Attacker dodges an attack or performs a Well-Timed block all their Poison Debuffs and Passives are removed."
        }
    }
    "status": 200,
    "detail": "Successful"
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/nodes/:id" baseUrl="https://api.rexians.tk" summary="Gets specific node info" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="id" type="int" required="true" %}
Id of node
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Successful response for specific node" %}
```javascript
{
    "node_id": "485",
    "node_name": "Singularity",
    "node_info": "Crit after 5 attacks instead of 7.",
    "status": 200,
    "detail": "Successful"
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Node id not found" %}
```javascript
{
    "detail": "400: Node id 10000 not found in the API Database"
}
```
{% endswagger-response %}
{% endswagger %}
