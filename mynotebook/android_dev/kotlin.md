# Kotlin language

variables typés:
var nomVariable: Type

Les types
- Nombres entier : Byte, Short, Int, Long
- Nombre décimal: Float, Double
- N'importe quel type de nombre: Number

- Logique: Booléen
- Caratère: Char (e.g. 'a','b')
- Chaine de caractères: String (e.g. "hello")

```{code-cell}
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
