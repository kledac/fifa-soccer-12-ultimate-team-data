![FIFA 12 Player Database](http://i.imgur.com/gUxon.png)

# FIFA Ultimate Team 2012 Data - Basic Edition

FIFA Ultimate Team exposes all player data via publicly accessible web services. This repository is here to help you build *your* ultimate team and will show you who the tallest player is, the fastest, the best overall, etc.

99.9% of those reading will be interested in this and nothing else: [player-database.csv](https://raw.github.com/leereilly/fifa-soccer-12-ultimate-team-data/master/player-database.csv). It's a database of a the UT players and their stats. If you have no idea what a CSV file, you can open it in Excel, Numbers or in Google Docs / [Zoho Sheet](https://sheet.zoho.com).

# FIFA Ultimate Team 2012 Data - Neckbeard Edition

All of the data can be found in the repository [here](https://github.com/leereilly/fifa-soccer-12-ultimate-team-data/tree/master/data).

## Players

### Player Images

Every asset (players, clubs, kits, etc) in the game has a unique identifier. Identifiers remain the same regardless of the season.

Let's take Maurice Edu as an example. He's an American midfielder currently playing for Rangers FC, the most successful club in the world. Maurice was on the cover of the American version of FIFA '09. He's also my 4-year old son's favorite player.

Mo's FIFA player ID is 179686, so we can grab his image from the 2012, 2011 and 2010 data set with the following URLs:

```
http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/images/players/web/179686.png
http://cdn.content.easports.com/fifa/fltOnlineAssets/2011/fut/items/images/players/web/179686.png
http://cdn.content.easports.com/fifa/fltOnlineAssets/2010/fut/items/images/players/web/179686.png
```

![Maurice Edu 2010](http://i.imgur.com/D9pTc.png)
![Maurice Edu 2011](http://i.imgur.com/Qph7i.png)
![Maurice Edu 2012](http://i.imgur.com/W6n3n.png)

### Player data

Player data is sent to the client (FIFA ultimate team on your XBOX, PS3, PC, or browser) in JSON e.g.

`http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/web/179686.json`

```javascript
{
  "Player": {
    "FirstName": "Maurice",
    "LastName": "Edu",
    "CommonName": null,
    "Height": "183",
    "DateOfBirth": {
      "Year": "1986",
      "Month": "4",
      "Day": "18"
    },
    "PreferredFoot": "Right",
    "ClubId": "86",
    "LeagueId": "50",
    "NationId": "95",
    "Rating": "66",
    "Attribute1": "79",
    "Attribute2": "61",
    "Attribute3": "64",
    "Attribute4": "67",
    "Attribute5": "67",
    "Attribute6": "78",
    "Rare": "0",
    "ItemType": "PlayerM"
  }
}
```

Most of these fields are self-explanatory, but they're detailed below:

* **Attribute1:** pace for outfield players; diving for goalkeepers
* **Attribute2:** shooting for outfield players; handling for  goalkeepers
* **Attribute3:** passing for outfield players; kicking for goalkeepers
* **Attribute4:** dribbling for outfield players; ref for goalkeepers
* **Attribute5:** defending for outfield players; speed for goalkeepers
* **Attribute6:** heading for outfield players; positioning for goalkeepers
* **Rare:** No longer used
* **ItemType:** This tells us whether the player's a goalkeeper (PlayerGk), defender (PlayerD), midfielder (PlayerM), or an attacking player (PlayerA).


## Kits

### Home

![](http://i.imgur.com/2s1bV.png)

Image: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/images/kits/web/j0_00086.png`

Data: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/web/6300263.json`

```javascript
{
  "Kit": {
    "ClubId": "86",
    "LeagueId": "50",
    "NationId": "42",
    "Rating": "73",
    "Rare": "1",
    "Category": "2",
    "Desc": "TeamName_Abbr15_86",
    "BioDesc": "Rangers",
    "ItemType": "Kit"
  }
}
```

### Away

![](http://i.imgur.com/tMoa6.png)

Image: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/images/kits/web/j1_00086.png`

Data: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/web/6400263.json`


```javascript
{
  "Kit": {
    "ClubId": "86",
    "LeagueId": "50",
    "NationId": "42",
    "Rating": "73",
    "Rare": "1",
    "Category": "3",
    "Desc": "TeamName_Abbr15_86",
    "BioDesc": "Rangers",
    "ItemType": "Kit"
  }
}
```

## Badges

![](http://i.imgur.com/H8hNy.png)

Image: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/images/clubbadges/web/s86.png`

Data: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/web/6000263.json`

```javascript
{
  "Badge": {
    "ClubId": "86",
    "LeagueId": "50",
    "NationId": "42",
    "Rating": "73",
    "Category": "1",
    "ItemType": "Badge",
    "Rare": "1"
  }
}
```

## Stadia

![](http://i.imgur.com/FEbBA.jpg)

Image: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/images/stadiums/web/249.jpg`

Data: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/web/6200054.json`

```javascript
{
  "Stadium": {
    "Rating": "74",
    "Rare": "0",
    "StadiumId": "249",
    "Name": "British Modern",
    "Cap": "20000",
    "Boost": "5",
    "ItemType": "Stadium"
  }
}
```

## Staff

## Managers

![](http://i.imgur.com/He8Bd.png)

Image: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/images/players/web/heads_staff_1000408.png`

Data: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/web/1000408.json`

```javascript
{
  "Manager": {
    "FirstName": "Alex",
    "LastName": "Ferguson",
    "NationId": "42",
    "Value": "83",
    "Rare": "1",
    "Weight": "15",
    "FormationId": "17",
    "TalkRating": "0",
    "Negotiation": "3",
    "AssetId": "1000408",
    "ItemType": "Manager"
  }
}
```

## Head Coaches

![](http://i.imgur.com/IEXtu.png)

Image: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/images/players/web/heads_staff_2000021.png`

Data: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/web/2000021.json`

```javascript
{
  "HeadCoach": {
    "FirstName": "S",
    "LastName": "Kitchen",
    "Rating": "77",
    "Rare": "0",
    "Attr": "4",
    "Amount": "10",
    "ItemType": "HeadCoach"
  }
}
```

## Goalkeeper Coaches

![](http://i.imgur.com/sPjKc.png)

Image: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/images/players/web/heads_staff_9000021.png`

Data: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/web/9000021.json`

```javascript
{
  "GkCoach": {
    "FirstName": "D",
    "LastName": "Gustafo",
    "Rating": "64",
    "Rare": "1",
    "Attr": "3",
    "Amount": "5",
    "ItemType": "GkCoach"
  }
}
```

## Fitness Coaches

![](http://i.imgur.com/tjMs7.png)

Image: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/images/players/web/heads_staff_3000004.png`

Data: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/web/3000004.json`

```javascript
{
  "FitnessCoach": {
    "FirstName": "A",
    "LastName": "Bachman",
    "Rating": "55",
    "Rare": "0",
    "Pos": "2",
    "PosBonus": "3",
    "Amount": "1",
    "ItemType": "FitnessCoach"
  }
}
```

## Physios

![](http://i.imgur.com/GpzW5.png)

Image: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/images/players/web/heads_staff_4000022.png`

Data: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/web/4000022.json`

```javascript
{
  "Physio": {
    "FirstName": "Y",
    "LastName": "Santos",
    "Rating": "66",
    "Rare": "0",
    "Attr": "3",
    "Amount": "5",
    "ItemType": "Physio"
  }
}
```

## Balls

![](http://i.imgur.com/mJvly.png)

Image: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/images/balls/web/ball_20.png`

Data: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/web/8120011.json`

```javascript
{
  "Ball": {
    "Rating": "70",
    "Rare": "0",
    "Desc": "adidas Torfabrik",
    "AssetId": "20",
    "Manufacturer": "ManufacturerAdidas",
    "Name": "BallName_20",
    "ItemType": "Ball"
  }
}
```

## Training

Data: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/web/5003001.json`

```javascript
{
  "Training": {
    "Desc": "GK Diving Bronze",
    "Rating": "55",
    "Rare": "0",
    "Amount": "5",
    "ItemType": "TrainingGkDiving"
  }
}
```

## Healing

Data: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/web/5002002.json`

```javascript
{
  "Healing": {
    "Desc": "Fitness Player Silver",
    "Rating": "70",
    "Rare": "0",
    "Amount": "40",
    "ItemType": "FitnessPlayer"
  }
}
```

## Contracts

Image: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/images/various/web/5000008.png`

Data: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/web/5001009.json`

```javascript
{
  "Contract": {
    "Desc": "Staff Gold",
    "Rating": "80",
    "Rare": "0",
    "Bronze": "11",
    "Silver": "11",
    "Gold": "13",
    "ItemType": "ContractStaff"
  }
}
```

## Misc.

Data: `http://cdn.content.easports.com/fifa/fltOnlineAssets/2012/fut/items/web/5004001.json`

```javascript
{
  "Misc": {
    "Desc": "NumFreeCredits",
    "Rating": "60",
    "Rare": "0",
    "Amount": "200",
    "ItemType": "MiscCoins"
  }
}
```

# Fun discoveries

* Kristof Van Hout is the tallest player in the game. He's an OK goalkeeper, but a bit slow clumsy. I use him as a benchwarmer and only bring him on for last-minute corner kicks. Dude's taller than Crouch and connects with headers with the force of a thousand suns.

* Quero Is the smallest player in the game. Do it for the lulz.

# Please note

* Special edition cards are not tracked here
* You should not use/abuse the web services/API/URLs listed above - doing so will probably get you blacklisted on the FIFA servers and you'll find it hard to play online.

# Statto! Statto! Statto!

![](http://1.bp.blogspot.com/_LT6s-Qii7wA/TPAvrArnQFI/AAAAAAAAADc/a5KWrtZh2sY/s1600/Statto.jpg)