# How does a script work

First let's take a look at a simple script:

{% method %}
## Script Construction

My first method exposes how to print a message in JavaScript and Go.

{% sample lang="js" %}
Here is how to print a message to `stdout` using JavaScript.

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

{% sample lang="go" %}
Here is how to print a message to `stdout` using Go.

```go
fmt.Println("My first method")
```

{% common %}
Whatever language you are using, the result will be the same.

```bash
$ My first method
```
{% endmethod %}
