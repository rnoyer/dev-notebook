# Kotlin language

## Déclaration d'une variable
En Kotlin, les variables sont typées.
```
var nomVariable: Type
```
Les types:
- Nombres entier : Byte, Short, Int, Long
- Nombre décimal: Float, Double
- N'importe quel type de nombre: Number

- Logique: Booléen
- Caratère: Char (e.g. 'a','b')
- Chaine de caractères: String (e.g. "hello")

```
fun main() {
    var age: Int=5
    var name: String="Joe"
    println("$name a $age ans!")

    age = 10
    println("$name a $age ans!")
    
    age = age + 1
    println("string template simple: $name a $age ans!")
    println("string template complexe: ${name.uppercase()} a ${age+4} ans!")
    
    println("""Raw string trim:
    		>	Nom: $name
            >	Age: $age
    """.trimMargin(">"))
}
```
## Controle de flux
### Comparateurs
| En francais | En Kotlin |
| ----------- | ----------- |
| Egal | == |
| Différent | != |
| Strictement supérieur | > |
| Strictement inférieur | < |
| Supérieur ou égal | >= |
| Inférieur ou égal | <= |
|Adresse egale à | === |

### Opérateurs booléens
| En francais | En Kotlin |
| ----------- | ----------- |
| Et | && |
| Ou | \|\| |
| Non | ! |

### if/else
```
if (condition) {
    //code
}
```

```
if (condition1 et condition2) {
    //code
}
```

#### Exemple:
```
var age: Int = 10
if (age > 5 && age < 15) {
    println("")
}
```
### when