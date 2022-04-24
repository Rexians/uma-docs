---
description: Gets all chapters from acts where this champ is found
---

# /find

{% swagger method="get" path="/find/?champ={string}" baseUrl="https://api.rexians.tk" summary="Gets the chapters where this champ is found from Acts 1-7" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="champ" type="string" required="true" %}
Name of champion
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Successful response for find" %}
```javascript
{
    "name": "IRON MAN (INFINITY WAR)",
    "class": "Tech",
    "url_page": "https://auntm.ai/champions/ironman_movie/tier/2",
    "img_portrait": "https://mcoc.rexians.tk/assets/portraits/ironman_movie.png",
    "champid": "ironman_movie+2+1",
    "find": {
    "story_quests": {
        "act_1": [],
        "act_2": [],
        "act_3": [],
        "act_4": [],
        "act_5": [],
        "act_6": [
            "6.1.1",
            "6.1.2",
            "6.1.4",
            "6.1.6",
            "6.2.1",
            "6.2.2",
            "6.2.4",
            "6.2.5",
            "6.2.6",
            "6.3.4",
            "6.4.2",
            "6.4.4"
            ],
        "act_7": [
            "7.1.5",
            "7.2.3",
            "7.2.4",
            "7.3.4",
            "7.3.6",
            "7.4.2",
            "7.4.6"
            ]
        }
    },
    "status": 200,
    "detail": "Successful"
}
```
{% endswagger-response %}

{% swagger-response status="422: Unprocessable Entity" description="Missing query parameter" %}
```javascript
{
    "detail": "The following arguments are missing: champ"
}
```
{% endswagger-response %}

{% swagger-response status="404: Not Found" description="Champ not found " %}
```javascript
{
    "detail": "404: Data with the champid: asd doesn't exist in the API Database!"
}
```
{% endswagger-response %}
{% endswagger %}

