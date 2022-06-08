---
description: Emotes are probably the easiest cosmetic type to understand.
---

# Emotes

Emotes are stored in an object called an EID (Which stands for Emote ID)

We will use the Default Dance as an example here.



The EID of the Default Dance is `EID_DanceMoves`

This is the basic data structure for emote

```
/Game/Athena/Items/Cosmetics/Dances
└── EID_DanceMoves
    ├── Emote Animation
    │   └── Emote Sound Cue
    │       └── Emote Audio (.ogg) / Handling random emote sounds
    ├── Emote Rarity, Name, Description, Release Season
    └── Emote Icons (Large & Small)
```

This is also the [JSON](https://en.wikipedia.org/wiki/JSON) for the EID of the Default Dance:

It's pretty self explanatory of what each thing is.

Also for strings like "Dance Moves" for example have a Key, (in this case its `24B06ACB42B6A683B18A2A923892EA9A`). If there is a key it means it can be edited because this is the text Fortnite displays. The key is part of the Unreal Engine's [Localization Tools](https://docs.unrealengine.com/4.26/en-US/ProductionPipelines/Localization/LocalizationTools/) so strings can be changed depending on the user's language.

Also icons have a Small and a Large version. The large one ends with `-L` so it's easy to differentiate the two.

```javascript
[
  {
    "Type": "AthenaDanceItemDefinition",
    "Name": "EID_DanceMoves",
    "Properties": {
      "Animation": {
        "AssetPathName": "/Game/Animation/Game/MainPlayer/Montages/Emotes/Emote_DanceMoves.Emote_DanceMoves",
        "SubPathString": ""
      },
      "Rarity": "EFortRarity::Common",
      "DisplayName": {
        "Namespace": "",
        "Key": "24B06ACB42B6A683B18A2A923892EA9A",
        "SourceString": "Dance Moves"
      },
      "ShortDescription": {
        "Namespace": "",
        "Key": "1D4899814C98F0DA4C1152873535BB9F",
        "SourceString": "Emote"
      },
      "Description": {
        "Namespace": "",
        "Key": "6250C0414E9AF00E04EE61BEE274B603",
        "SourceString": "Express yourself on the battlefield."
      },
      "GameplayTags": [
        "Cosmetics.EmoteType.Dance",
        "Cosmetics.Source.DefaultItem",
        "Cosmetics.Filter.Season.1",
        "Phoebe.Cosmetic.Minus.Zone1",
        "Phoebe.Cosmetic.Minus.Zone2"
      ],
      "SmallPreviewImage": {
        "AssetPathName": "/Game/UI/Foundation/Textures/Icons/Emotes/T-Icon-Emotes-E-Dance.T-Icon-Emotes-E-Dance",
        "SubPathString": ""
      },
      "LargePreviewImage": {
        "AssetPathName": "/Game/UI/Foundation/Textures/Icons/Emotes/T-Icon-Emotes-E-Dance-L.T-Icon-Emotes-E-Dance-L",
        "SubPathString": ""
      }
    }
  }
]
```
