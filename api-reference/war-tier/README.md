---
description: Gets info about alliance war at specific tier
---

# /war/:tier

{% swagger method="get" path="/war/:tier" baseUrl="https://api.rexians.tk" summary="Gets alliance war info a specific tier" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" type="int" name="tier" required="true" %}
Tier of alliance war
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Successful response of alliance war at specific tier" %}
```javascript
{
    "tier": 4,
    "nodes": {
    "1": [
        "Steady Buildup - Fury",
        "Running On Fumes",
        "While They're Down - 1"
        ],
    "2": [
        "Ebb And Flow - KNOCK DOWN",
        "Right Back At It - 2",
        "Force of Will"
        ]
    }
    "difficulty": "Challenger",
    "tier_multiplier": "4.5",
    "tier_rank": "2%-3%",
    "status": 200,
    "detail": "Successful"
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Tier not found" %}
```javascript
{
    "detail": "Tier 44 not found in the file"
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Tier not of correct type" %}
```javascript
{
    "detail": "Incorrect type for parameter (tier). Should be integer"
}
```
{% endswagger-response %}
{% endswagger %}
