---
description: How to use find endpoint
---

# Fetching Find Response

The `find` endpoint allows the user to find where the champ is located from Acts 1-7. To use it, the endpoint is `https://api.rexians.tk/find` and the query parameter is `champ` , the same as the `champs` endpoint. To find the correct `champ` name, check out [Champ Codes](../../important-info/champ-codes.md). \
\
Here is an example with Immortal Abomination. The `find` endpoint would be\
`https://api.rexians.tk/find/?champ=ibom`\


{% tabs %}
{% tab title="Python" %}
```python
import requests        #pip install requests

#Get locations of Cosmic Ghost Rider from Acts 1-7
war = requests.get("https://api.rexians.tk/find/?champ=cgr").json()
```
{% endtab %}

{% tab title="Javascript" %}
```javascript
import fetch from "node-fetch"  //npm install node-fetch 

// Get locations of Iron Man Infinity War from Acts 1-7
fetch('https://api.rexians.tk/find/?champ=imiw')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(err => {
	console.error(err);
  });
```
{% endtab %}
{% endtabs %}
