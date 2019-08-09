# player

## Description
Returns data related to a player such as game stats, achievements, rank, etc.

## Parameters
- key
- uuid
- ~~name~~ _Deprecated_

## Example
It is important to note that there is a lot of data provided by this method, so not everything can be included in the example. Some of the more complex or important data has been included and duplicate, similar, or simple to understand data has not.

```js
{
	"success": true,
	"player": {
		"_id": "561bdd5fde314c0f04e813ae", // Unique ID of the user in the Hypixel database
    "achievements": { // List of tier achievements along with the progress made on them.
      "blitz_kills": 12000,
      "uhc_consumer": 201
      // ...
    },
    "achievementsOneTime": [ // Array of one-time achievements earned by the user.
      "general_first_join", 
      "walls_first_perk"
      // ...
    ],
    "channel": "ALL", // The channel this user has selected via /chat
    "chat": true, // Whether this user has chat enabled via /togglechat
    "displayname": "hypixel", // Last known username of this user (username they had when they last logged on)
    "firstLogin": 1379120630908, // Timestamp that this user first logged into the network. Logins before August 23rd, 2013 were not recorded.
    "fly": true, // Whether this user has fly enabled via /fly
    "knownAliases": ["hypixel"], // All of this user's username history
    "lastLogin": 1565305679604, // Timestamp that this user last logged into the network
    "networkExp" 9.2792488E7, // The amount of network EXP this user has
    "packageRank": "MVP", // Package rank this user purchased before the new Minecraft EULA
    "newPackageRank": "MVP_PLUS", // Package rank this user purchased after the new Minecraft EULA
    "monthlyPackageRank": "SUPERSTAR", // This user's current monthly package rank. Superstar == MVP++
    "rank": "ADMIN", // Staff/special rank applied to this user
    "rankPlusColor": "DARK_PURPLE", // The color of this user's MVP+/MVP++ plus color
    "monthlyRankColor": "GOLD", // The color selected by the user to display their MVP++ rank as
    "prefix": "§d[PIG§b++§d]", // Prefix of this user
    "parkourCompletions": { // Parkour completions completed by this user
			"ArcadeGames": [{ // Game this parkour was completed in
				"timeStart": 1425782715264, // Timestamp that the parkour was completed
				"timeTook": 137338 // Time taken in milliseconds to complete the parkour
			}, {
				"timeStart": 1448496963271,
				"timeTook": 6200
			},
      // ...
      ],
      // ...
    },
    "quests": {
			"blitzerk": {
				"completions": [{
					"time": 1473555566534
				},
        // ...
        ]
			},
			"explosive_games": {
				"active": {
					"started": 1450792668178,
					"objectives": {}
				}
			},
      // ...
    },
    "settings": { // Global account settings
			"allowFriendRequests": true,
			"allowGuildRequests": false,
			"profanityLevel": "WEAK_FILTER",
			"profanityLevel_PARTY": "STRONG_FILTER",
			"profanityLevel_PM": "WEAK_FILTER",
			"privateMessagePrivacy": "HIGH",
			"bridgeChallengePrivacy": "MAX",
      // ...
		},
		"spec_speed": 2, // Speed setting selected by this user in spectator mode
    "stats": { // Player stats for gamemodes
      "Arcade": {
        "coins": 1.264312E7, // Current coins in said gamemode
        "goals_soccer": 1823,
        // ...
      }, 
      "HungerGames": {
        "arachnologist": 4, // Level of the arachnologist kit
        "armorer": 9, // Level of the armorer kit
        // Kits...
        "kills": 1338,
				"exp_hunter": 34,
        "defaultkit": "Hunter", // Kit to choose when no kit is selected
        "HunterInventory": { // Custom inventory for the Hunter kit
					"0": "272,0", // Item ID in slot 0, followed by the data value
					"4": "373,16386",
          // ...
				},
        // ...
        "Walls": {
          "InventoryLayout2": { // inventory of this player
            "18": "383,92,NONAME, // Item ID of item in slot 18, followed by a data value, followed by a custom item name
            "19": "373,0,§r§fPotion of Fire Resistance",
          }
        },
        "GingerBread": {
          "engine_active": "{GingerbreadPart:{PartType:ENGINE,PartRarity:AWESOME,Attributes:[{KartAttributeType:RECOVERY,Level:5},{KartAttributeType:ACCELERATION,Level:5},{KartAttributeType:TOP_SPEED,Level:5}]}}", // Serialized engine data for the currently active kart
          // ...
        },
        "SkyWars": {
          "privategames": { // Private game settings for SkyWars games hosted by this user
            "enable_teleport_mayhem": false,
            "dragons": "5 Dragons",
            "health_buff": "Normal Health",
            "chest_armour": "Diamond Protection II",
            "chest_bows": "Punch II",
          },
          // ...
        },
        "MurderMystery": {
          "murdermystery_books": ["innocent", "detective"], // Introductory books read by this user
          // ...
        },
        "Pit": {
          "profile": {
            "last_save": 1561576678450, // Timestamp that this user's inventory was last saved
            "inv_enderchest": { // This user's enderchest inventory
              "type": 0,
              "data": [31, -117, 8, 0, 0, 0, 0, /* ... */] // gzipped NBT data of this user's inventory
            }, 
            // ...
          }, 
          // ...
        }, 
        // ...
      },
      // ...
    },
    // ...
  }
}
```
