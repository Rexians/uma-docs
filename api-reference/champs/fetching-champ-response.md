---
description: How to use champ endpoint
---

# Fetching Champ Response

The `/champs` endpoint requires 3 query params- `champ` ,`tier` and `rank`. For example, if you want to get info about **tier 6 Abomination of rank 4**, the URL will be `https://api.rexians.tk/champs/?champ=abomination&tier=6&rank=4`

The champion names are found in [Champ Codes](../../important-info/champ-codes.md). To use, look for the champion you would like to search and find it's corresponding champ code. This champ code will be used in the `champ` parameter. For example, for **Imortal Abomination** the champ code is **ibom.** For a 3 star at rank 2, the request would be `https://api.rexians.tk/champs/?champ=ibom&tier=3&rank=2`&#x20;

The tiers and rank have restrictions. Tiers cannot be higher than 6 and rank cannot be higher than 5. However, there are combinations that are also not possible. For example, a tier 1 champ cannot be rank 5. For all the tier and rank info, check out [Tiers/Rank Info](https://app.gitbook.com/s/wZCpADmfIdYTpf0r2RHV/\~/changes/7fX0WEhoItcZ7PuGkyp8/important-infos/tiers-ranks-info).

Example to use the `/champs` endpoint in some langauges is shown below:

{% tabs %}
{% tab title="Python" %}
```python
import requests

champ_name = str(input("Write champname: "))
tier = int(input("Write Tier of Champion: "))
rank = int(input("Write Rank of Champion: "))
url = f"https://api.rexians.tk/champs/?champ={champ_name}&tier={tier}&rank={rank}"

response = requests.request("GET", url)
print(response.text)
```
{% endtab %}

{% tab title="Javascript" %}
```javascript
import fetch from "node-fetch"  //npm install node-fetch 

//Get all nodes
fetch('https://api.rexians.tk/champs/?champ=ibom&tier=3&rank=2')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(err => {
	console.error(err);
  });
```
{% endtab %}
{% endtabs %}

