# How does a script work

First let's take a look at a simple script:

```js
function maCustom() {
  console.log(`J'ai ${API.character.kamas()} kamas.`);
}
const config = {
  "MAX_PODS": 90,
  "GATHERS": [31, 38]
};
const move = [
  {
    map: 8765242,
    gather: true,
    fight: true,
    direction: "top"
  }, {
    map: "-2,0",
    direction: "top|bottom"
  }, {
    map: "-2,0",
    custom: maCustom,
    direction: "right"
  }
];
const bank = [
  {
    map: 8765242,
    direction: "bottom"
  }
];
const phenix = [
  {
    map: 8765242,
    direction: "bottom"
  }
];
```

What we need to remember is that a script has three **States** which have to always be present: **move**, **bank**, **phoenix**.

######  move

    move is to represent the maps where the bot will roam for gathering ressources or fighting.

###### bank

    bank is to represent which bank the character will go to when `"MAX_PODS"` is reached.

###### phoenix

    phoenix is to represent which phoenix the character will go when he is in phantom mode.







