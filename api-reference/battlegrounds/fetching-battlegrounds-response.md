---
description: How to use battlegrounds endpoint
---

# Fetching Battlegrounds Response

The battlegrounds endpoint let's us get information about the current season for battlegrounds. To use it, make a request to the endpoint `http://api.rexians.tk/battlegrounds/season/:season` where `:season` is the path parameter. We are only storing information from season 4 and up at this time.

Here is an example of what the battlegrounds for season 4 request would look like. \``` http://api.rexians.tk/battlegrounds/season/4` ``

{% tabs %}
{% tab title="Python" %}
```python
import requests        #pip install requests
import json

#Get battlegrounds info for season 4
bg = requests.get("http://api.rexians.tk/battlegrounds/season/4").json()
```
{% endtab %}

{% tab title="Javascript" %}
```javascript
import fetch from "node-fetch"  //npm install node-fetch 

fetch('http://api.rexians.tk/battlegrounds/season/4')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(err => {
	console.error(err);
  });
```
{% endtab %}
{% endtabs %}
