## Script Custom Function

With the **Script Engine** there is the possibility use **custom functions**. This gives the user a chance to really cutomize how scripts works and to use the extensive **Cookie Touch Bot API**.

[Cookie Touch Bot API](https://github.com/Ehstrali/markdownedit "Cookie Touch Bot API")

{% method %}

Before using an instruction from the API you need to remember to use the keyword **yield** as follows.

{% sample lang="js" %}
```js
yield* npc.npc(-2, 1)
```

{% endmethod %}

For this we will take a look at a custom function to talk to the NPC to go from **Incarnam** to **Astrub**.

{% sample lang="js" %}
```js
// Call sutom function on map
{ map: 80220676, custom: function* () {
    // Talk to NPC -2 and choose the first option (1)
    yield* npc.npc(-2, 1)
    // If we are in dialog
    if (isInDialog()) {
      // Print the following message
      printMessage("Talking to go to Astrub.")
      // Choose reply -1
      yield* npc.reply(-1)
      // Choose reply -1
      yield* npc.reply(-1)
    }
  }}
```

We can see in this short example the power of the **Script Engine** and how far custom functions can go from exchange to bidding to many more.




