# TypeScript basics

## Les types

### Primitifs
Les types primitifs sont les types les plus couramment utilisés : `string`, `number`, `boolean`

TS a également un type `any` qui permet d'éviter les erreurs de type check.

## Typage explicite
Les variables sont typées comme suit. Cependant ce n'est généralement pas nécessaire puisque TS déduit le type en fonction du contenu de la variable.

```ts
const name: string = "Jean";

const message = "Coucou";
// TS déduira >> const message: string

```

Les paramètres de fonctions peuvent être typées simplement

```ts
function sayHello(name: String, date: Date){
  console.log(`Hello ${name}, today is ${date.toDateString()}`)
}

sayHello("Bob", Date()) // [❎] Argument of type 'string' is not assignable to parameter of type 'Date'.

sayHello("Bob", new Date()) // [✅]
```
## Les Arrays
Il est possible de typer les arrays, notamment leur contenu.
Exemple:
```ts
// un array contenant des nombres
number[]

// Ecriture alternative de forme T<U>
Array<number>
```
## Les fonctions
Comme vu plus haut, il est possible de typer les paramètres, mais il est également possible de typer la sortie d'une fonction:
```ts
function getNumber(): number {
  return 23;
}
```
### Fonction qui retourne une promesse
Utiliser le type `Promise`
```ts
await function getNumber(): Promise<number> {
  return 23;
}
```

## Type Objet
```ts
function printCoord(pt: {x:number, y:number}){
  console.log(`x coord are ${pt.x}`);
  console.log(`y coord are ${pt.y}`);
}

printCoord({x: 4, y:5});
```

Une propriété peut être optionnelle.
Appeler la propriété d'un objet qui n'existe pas retourne `undefined`. Ainsi, dans le cas d'une propriété optionnelle, l'exception doit être gérée.

```ts
function printName(infos: {firstName: string, lastName?: string}){
  // Below, '?' handle the exception
  console.log(infos.lastName?.toUpperCase());
}
```

## Union Types
Il est possible d'unir plusieurs types pour en créer un nouveau.
```ts
function printId(id: number | string){
  console.log(`my ID is ${id}`)
}

printId('242') // [✅]
printId(234) // [✅]
printId({id: 434}) // [❎]
```
Ici, le parametre id accepte les `number` et les `string`.
TS n'autorisera uniquement des opérations valable pour l'ensemble des types de l'union. Pour effectuer des opérations spécifiques a un type, il faut 'réduire' l'union a l'aide du code.

Par exemple en utilisant `typeof`:
```ts
function printId(id: number | string) {
  if (typeof id === "string") {
    // In this branch, id is of type 'string'
    console.log(id.toUpperCase());
  } else {
    // Here, id is of type 'number'
    console.log(id);
  }
}
```
Ou une fonction comme `Array.isArray`
```ts
function welcomePeople(x: string[] | string) {
  if (Array.isArray(x)) {
    // Here: 'x' is 'string[]'
    console.log("Hello, " + x.join(" and "));
  } else {
    // Here: 'x' is 'string'
    console.log("Welcome lone traveler " + x);
  }
}
```
## Les Alias
Les alias permettent de nommer des types custom (ou non).
Voici quelques exemples:
```ts
type Point: {
  x: number;
  y: number;
}

type Id: number | string

type Dummie: number
```

## Les interfaces
Les interfaces sont une autre manière de déclarer un type `object`
```ts
interface Point {
  x: number;
  y: number;
}
```
Les types `Object` et les interfaces sont très similaires et peuvent être utilisées indiféremment dans la plupart des cas.

La différence entre les deux est que, une `interface` peut être changée et étendue, à l'instar des `types`.

## Assertions de type
```ts
const myCanvas = document.getElementById("main_canvas") as HTMLCanvasElement;
const myCanvas = <HTMLCanvasElement>document.getElementById("main_canvas");
```

## Types litérals
Une variable `const` ne change jamais de valeur. Ainsi, pour TS, sont type sera la valeur en question: 

```ts
const age = 33
age; // TS déduit que le type de age est '33' 
```

Tel quel, cela n'est pas utile. Cependant, il est possible de faire des unions de litéraux. Ainsi, on peut définir un set de valeurs:
```ts
function printText(s: string, alignment: "left" | "right" | "center") {
  // ...
}
printText("Hello, world", "left");
printText("G'day, mate", "middle"); // TS retourne une erreur car 'middle' ne fait pas partie du type du paramètre 'alignement'
```
Il peut également s'agir de nombres.

L'union permet de lier des literaux et des non-litéraux (`number`, `interface`, etc.)

## `null` et  `undefined`
### Opérateur d'assertion non-null
Il est possible de supprimer `null` et `undefined` d'un type sans faire de check explicite en écrivant `!` juste après une expression.
```ts
const age = 33
function liveDangerously(x?: number | null) {
  // No error
  console.log(x!.toFixed());
}
```
A n'utiliser que quand la valeur ne peut pas être `null` ou `undefined`.
