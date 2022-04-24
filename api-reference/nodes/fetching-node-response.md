---
description: How to use node endpoint
---

# Fetching Node Response

There are 100s of nodes used in MCOC. Each node has a name and what it does. To get this info, make the request to the endpoint `https://api.rexians.tk/nodes`. This will give a list of nodes we currently have data for.&#x20;

To get the information for a specific node, use the id that was found in the previous request. For example, `"A Good Defense"` node has id of 1. To get just the info of this node, request at `https://api.rexians.tk/nodes/1`.

{% tabs %}
{% tab title="Python" %}
```python
import requests       #pip install requests
import json

#Gets all nodes
nodes = requests.get("https://api.rexians.tk/nodes").json()

#Gets node with id 324
node = requests.get("https://api.rexians.tk/nodes/324").json()
```
{% endtab %}

{% tab title="Javascript" %}
```javascript
import fetch from "node-fetch"  //npm install node-fetch 

//Get all nodes
fetch('https://api.rexians.tk/nodes')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(err => {
	console.error(err);
  });

//Get node 324
fetch('https://api.rexians.tk/nodes/324')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(err => {
	console.error(err);
  });
```
{% endtab %}
{% endtabs %}
