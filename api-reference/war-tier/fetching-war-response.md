---
description: How to use war endpoint
---

# Fetching War Response

Alliance war in the game has various info that is provided with this endpoint. To use, request at the given route with a viable tier. For example, to get info for tier 7, make a request to `https://api.rexians.tk/war/7`. This will give a response with tier, nodes, difficulty, tier multiplier, and tier rank. \
Note - The highest possible tier is 22

{% tabs %}
{% tab title="Python" %}
```python
import requests        #pip install requests
import json

#Get war info for tier 10
war = requests.get("https://api.rexians.tk/war/10").json()
```
{% endtab %}

{% tab title="Javascript" %}
```javascript
import fetch from "node-fetch"  //npm install node-fetch 

fetch('https://api.rexians.tk/war/10')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(err => {
	console.error(err);
  });
```
{% endtab %}
{% endtabs %}
