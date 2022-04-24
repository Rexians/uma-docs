---
description: Endpoint for getting basic champs info.
---

# /champs

{% swagger method="get" path="champs/?champ={string}&tier={int}&rank={int}" baseUrl="https://api.rexians.tk/" summary="Champ name must follow API champ code and tiers/rank have restrictions. Find more in Champ Codes and Tiers/Ranks Info" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="champ" type="string" required="true" %}
Name of champion
{% endswagger-parameter %}

{% swagger-parameter in="query" name="tier" type="int" required="true" %}
Tier of champion
{% endswagger-parameter %}

{% swagger-parameter in="query" name="rank" type="int" required="true" %}
Rank of champion
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Successful response for champ stats" %}
```javascript
"{
  "rank": 3,
  "prestige": "4301",
  "hp": "16420",
  "attack": "1265",
  "crit_rate": "299",
  "crit_dmge": "632",
  "armor": "198",
  "block_prof": "5018",
  "energy_resist": "0",
  "physical_resist": "0",
  "crit_resist": "0",
  "sig_info": "The Powerlock Debuff triggered when reaching 5 Judgments is upgraded to a Damnation Debuff dealing 670.64 to 1582.1 damage over 6 seconds. Opponents under Damnation are also Power Locked, Heal Blocked, and Fate Sealed, all of which are unaffected by Ability Accuracy modifications.",
  "url_page": "https://auntm.ai/champions/ghostrider_cosmic/tier/5",
  "champid": "ghostrider_cosmic+5+3",
  "challenger_rating": 100,
  "Abilities": {
      "PASSIVE": [
          "A lack of blood provides full immunity to Bleeding.",
          "Being wreathed in Hellfire provides full Immunity to Incinerate",
          "When fighting a #Villain, at the start of the fight gain a 100% Chance to place an indefinite Armor Break Debuff on the Opponent reducing their Armor Rating by 666.67, and removing an active Armor Up Buff."
        ],
      "COSMIC JUDGMENTS - PASSIVE": [
          "When Cosmic Ghost Rider triggers Armor Up, Fury, Precision, Cruelty, Power Gain, Unblockable, Vigilance, or Aptitude Buffs he also has a 100% chance to place a corresponding Judgment on his Opponent.",
          "Each Judgment can only be stacked a single time, but lasts indefinitely.",
          "Each Judgment placed on the Opponent increases the duration of any Buff Triggered on Cosmic Ghost Rider by 20%. While you have 5 Judgments in place, this bonus is doubled.",
          "Upon gaining any 5 or more Judgments there is a 100% chance to place a Power Lock Debuff on the Opponent for 6 seconds.",
          "After this Power Lock ends or if it fails to apply, all Judgments on the Opponent have a 100% chance to be converted into to Armor Break Debuffs, each reducing Armor Rating by 500 for 10 seconds, and removing an Armor Up Buff.",
          "If Cosmic Ghost Rider gains a Fate Seal Debuff, he Removes all of his Judgments, and he cannot trigger new ones until it ends."
        ],
      "WHEN ATTACKED": [
          "When Struck if the Judgment of Armor is not active: 100% Chance to trigger an Armor Up Buff granting +857.14 Armor for 10 seconds."
        ],
      "FINISH A 5 HIT COMBO WITH A MEDIUM ATTACK": [
          "If the Judgment of Vigilance is not active: 100% Chance to trigger a Vigilance Buff, preventing your attacks from Missing for 10 seconds."
        ],
      "FINISH A 5 HIT COMBO WITH A LIGHT ATTACK": [
          "If the Judgment of Power Gain is not active: 100% Chance to trigger a Power Gain Buff, granting 75% of a Bar of Power over 1.25 seconds."
        ],
      "WHEN CHARGING A HEAVY ATTACK": [
          "If the Judgment of Aptitude is not active, he has a 100% Chance to trigger an Aptitude Buff increasing the potency of any Armor Up, Fury, Cruelty, and Precision Buffs triggered by 50% for 8 seconds."
        ],
      "SPECIAL ATTACKS": [
          "If the Judgment of Cruelty is not active: 100% Chance to trigger a Cruelty Buff, increasing Critical Damage Rating by 702.7 for 10 seconds."
        ],
      "SPECIAL ATTACK 1": [
          "On Activation if the Judgment of Unblockable is not active: 100% Chance to trigger an Unblockable Buff for 1 seconds.",
          "This attack Incinerates the enemy, dealing 759 Energy Damage over 5 seconds. This effect also removes Perfect Block Chance and reduces Block Proficiency by 50% while it's active."
        ],
      "SPECIAL ATTACK 2": [
          "On Activation if the Judgment of Precision Is not active: 100% Chance to trigger an Precision Buff increasing Critical Rating by 8000 for 10 seconds.",
          "100% chance to inflict an Armor Break Debuff, removing 1 Armor Up Buff and reducing Armor Rating by 1636.36 for 15 seconds."
        ],
      "SPECIAL ATTACK 3": [
          "On Activation if the Judgment of Fury is not active: 100% Chance to trigger an Fury Buff increasing Attack by 1581.25 for 15 seconds."
        ]
      }
    }
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Tier not in restriction" %}
```javascript
{
    "detail": "400: Tier should not be above 6"
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Incorrect combination of tier and rank (For all tiers/ranks)" %}
```javascript
{
    "detail": "400: Rank of a 1 star should not be above 3."
}
```
{% endswagger-response %}

{% swagger-response status="404: Not Found" description="Champion not found" %}
```javascript
{
    "detail": "404: Data with the champid: asd doesn't exist in the API Database!"
}
```
{% endswagger-response %}
{% endswagger %}
