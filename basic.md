## Script Header

{% method %}

This script header is probably the most important part of the script. This will let the dev team add your script to the **public script repositery** where other users will be able to download and use scripts as well as vote if it works well or not.

{% sample lang="js" %}
```js
//Title: Incarnam To Astrub
//Version: 1.0.0
//Type: 1
//Tags: path, incarnam, astrub
//Description: This is a script that is made to bring you from Incarnam to Astrub.
```
{% endmethod %}

## Script Details

First let's take a look at a sample script and see how it is structured.

What we need to remember is that a script has three **States** which you'll need most of the time: **move**, **bank**, **phoenix**. And also you will need to use the **config**.

###### config

* config is to define the number of `"MAX_PODS"` and the ressources to farm `"ELEMENTS_TO_GATHER"` and all other configuration parameters.

{% sample lang="js" %}
```js
const config = {
  MAX_PODS: 90,
  ELEMENTS_TO_GATHER: [ 75, 71, 74, 77, 76, 78, 79, 81, 264, 263 ],
  OPEN_BAGS: true
}
```
PS: `MAX_PODS` is defined as a **percentage**.
###### move

* move is to represent the maps where the bot will roam for gathering ressources or fighting.

{% sample lang="js" %}
```js
const move = [
  { map: "11,10", path: "top" },
  { map: "11,9", path: "right" },
  { map: "12,9", path: "top", gather: true },
  { map: "12,8", path: "right", gather: true },
  { map: "5,-19", fight: true, path: "right" },
  { map: "6,-19", fight: true, path: "left" }
]
```
###### bank

* bank is to represent which bank the character will go to when `"MAX_PODS"` is reached.

{% sample lang="js" %}
```js
const bank = [
  { map: "12,8", path: "right" },
  { map: 88081177, door: 216 }, // Map extérieure de la banque
  { map: 99095051, npcBank: true, path: "410" } // Map intérieure de la banque
]
```

###### phoenix

* phoenix is to represent which phoenix the character will go when he is in phantom mode.

{% sample lang="js" %}
```js
const phenix = [
  { map: "11,10", path: "top" },
  { map: "11,9", path: "right" },
]
```

###### comments

In the scripts you have the possibility to use comments. The Script Engine being based in JavaScript comments work as follow with a double slash `//`.
{% sample lang="js" %}
```js
// This line will be ignored.
```





###### example

This is example is a non functionning script it is simply to show and share the syntax


{% sample lang="js" %}
```js
//Title: Incarnam To Astrub
//Version: 1.0.0
//Type: 1
//Tags: path, incarnam, astrub
//Description: This is a script that is made to bring you from Incarnam to Astrub.
const config = {
  MAX_PODS: 90,
  ELEMENTS_TO_GATHER: [ 75, 71, 74, 77, 76, 78, 79, 81, 264, 263 ],
  OPEN_BAGS: true
}
const move = [
  { map: "11,10", path: "top" },
  { map: "11,9", path: "right" },
  { map: "12,9", path: "top", gather: true },
  { map: "12,8", path: "right", gather: true },
  { map: "5,-19", fight: true, path: "right" },
  { map: "6,-19", fight: true, path: "left" }
]
const bank = [
  { map: "12,8", path: "right" },
  { map: 88081177, door: 216 }, // Map extérieure de la banque
  { map: 99095051, npcBank: true, path: "410" } // Map intérieure de la banque
]
const phenix = [
  { map: "11,10", path: "top" },
  { map: "11,9", path: "right" },
]

```
{% endmethod %}
