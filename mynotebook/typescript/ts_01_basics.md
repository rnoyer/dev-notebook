# TypeScript basics

## Les types

### Primitifs
Les types primitifs sont les types les plus couramment utilisés : `string`, `number`, `boolean`

TS a également un type `any` qui permet d'éviter les erreurs de type check.

### Les Arrays
Il est possible de typer les arrays, notamment leur contenu.
Exemple:
```ts
// un array contenant des nombres
number[]

// Ecriture alternative de forme T<U>
Array<number>
```

## Typage explicite
Les variables sont typées comme suit. Cependant ce n'est généralement pas nécessaire puisque TS déduit le type en fonction du contenu de la variable.

```ts
const name: string = "Jean";

const message="Coucou";
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
