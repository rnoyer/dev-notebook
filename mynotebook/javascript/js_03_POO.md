# Javascript Object Oriented Programation
 
 ## Create an object
 There is three ways to create an object:

### Literal object
```js
const Me = {
    firstName: "Romain",
    lastName: "Noyer",
    getFullName: () => `${Me.firstName} ${Me.lastName}`,
    sayHello: () => console.log("Hello there")
}

// Return first name and last name
console.log(Me.getFullName())

// Says Hello There
Me.sayHello()
```

### Using a Prototype
```js
function Me(firstName, LastName) {
    this._firstName = firstName
    this._lastName = lastName

}

Me.prototype.getFullName = function() {
    return `${Me.firstName} ${Me.lastName}`,
}

Me.prototype.sayHello = function() {
    console.log("Hello There")
}

// Instanciate new Me
const Romain = new Me("romain","noyer")
// Return first name and last name
console.log(Romain.getFullName())
// Says Hello There
Romain.sayHello()
```

### Using 'class' keyword
```js
class Me {
   constructor(firstName, lastName) {
       this._firstName = firstName
       this._lastName = lastName
   }

   getFullName() {
       return `${this._firstName} ${this._lastName}`
   }

   sayHello() {
       console.log("Hello There")
   }
}

// Instanciate new Me
const Romain = new Me("romain", "noyer")
// Return first name and last name
console.log(Romain.getFullName())
// Says Hello There
Romain.sayHello()
```

## Object inheritance
Allow an objet to be 'upgraded' with all atributes and methods of another object.

