# Javascript Object Oriented Programation

## Constructor function
```js
function HouseKeeper(name,experience,cleaningRep) {
    this.name = name;
    this.experience = experience;
    this.cleaningRep = cleaningRep;
}
```

## Initialize object
```js
var houseKeeper1 = new HouseKeeper("Sandra", 3,["bath","bed","lobby"]);

var houseKeeper2 = new HouseKeeper("Pedro", 10,["floor","roof","wall"]);
```
