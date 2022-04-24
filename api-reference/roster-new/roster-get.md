# /roster/get

**BASE URI:** `https://rexians.tk/roster/get`

This is a route which is kind of connected to Discord. It shows the champs and some other information about the user.

* **Query Params**->
  * 1- `gamename`
* **Overview**
  * This endpoint is used to get the information of a user who is registered in the [Rexians Web](https://mcoc.rexians.tk/login).
  * The `roster.get` endpoint needs one query parameters- `gamename` which is a gamename user specified while logging in for the first time in the Web.
  * Ex. To get the info on user of gamename: `The Indominus`, the URI will be `https://api.rexians.tk/roster/get?gamename=The Indominus`
* **Response**
  * Example of Successful response of `The Indominus`(200 OK)
    * ```
         {
         "game_name": "The Indominus",
         "discord_id": 706033276493758600,
         "avatar_url": "https://cdn.discordapp.com/avatars/706033276493758545/76219b3a57f0a57f52b72eeaf4ae89ab.png",
         "prestige": 7225,
         "roster": [
             {
             "champ_name": "HYPERION",
             "tier": 5,
             "rank": 5,
             "prestige": 7225,
             "sig_number": 100,
             "img_link": "https://auntm.ai/resources/ui/uigacha/featured/gachachaseprize_256x256_hyperion.png",
             "champid": "hyperion+100+5+5",
             "url_page": "https://auntm.ai/champions/hyperion/tier/5"
             }
         ],
         "status": 200,
         "detail": "Successful"
         }
      ```

Example of Unsuccessful response(404 Not Found)

* ```
    {"detail":"Player with this name doesn't exists."}
  ```
