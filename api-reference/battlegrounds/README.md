---
description: Gets info about battlegrounds for season
---

# /battlegrounds

{% swagger method="get" path="/battlegrounds/season/:season" baseUrl="https://api.rexians.tk" summary="Gets battleground info for specified season" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="season" type="int" required="true" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Successful response for battlegrounds" %}
```javascript
{
    "start": "",
    "end": "",
    "season": 0,
    "victory_track" : 
    {
        "ranks" : [],
        "rewards" : {},
        "nodes" : []
    },
    "gladiator_circuit" : 
    {
        "ranks" : [],
        "rewards" : {},
        "nodes" : []
    },
    "status": 200,
    "detail": "Successful"
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Season below 4 not available" %}
```javascript
{
    "detail": "Season below 4 not available."
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Season parameter not integer" %}
```javascript
{
    "detail": "Incorrect type for parameter (season). Should be integer"
}
```
{% endswagger-response %}
{% endswagger %}
