##Prework

``` swift
// COMPLEX TYPES 

// Arrays
// Se escriben entre corchetes y es posible que sean de cualquier tipo de dato
// [String], [Int], [Double], [Bool]
 // Beatles example
 let john = "John Lennon"
 let paul = "Paul MacCartney"
 let george = "George Harrison"
 let ringo = "Ringo Starr"

 let beatles = [john, paul, george, ringo]
 print(beatles)
 // Es posible accesar a una parte del arreglo usando su posición 
 print(beatles[1])
 // No hacer: Tratar de accesar a una parte del arreglo que no existe
 // print(beatles[9])

 // Sets
 // Son similares a los arreglos con la diferencia de que no repiten valores 
 // (los guardan solo una vez) y no guardan los valores en ningún orden
let colors = Set(["red", "green", "blue"])
print(colors)
// Los valores repetidos son ignorados
let colors2 = Set(["red", "green", "blue", "red", "blue"])
print(colors2)

// Tuplas
// Tipo de dato que permite guardar multiples valores (diferentes o no) en un 
// mismo dato. Las tuplas:
// * Son fijas en valor (no puede cambiar sus conceptos o sus tipos)
// * Es posible accesar a cada concepto de la tupla por medio de su posicion 
// o de su nombre (si no existen, no se pueden accesar a ellos)
var name = (first: "Taylor", last: "Swift")
print(name)
// Acceso por posición
print(name.0)
// Acceso por nombre
print(name.first)
name.0 = "Miry"
print(name.0) 
// name.0 = 24 debería ser erroneo, por que name.0 es y será siempre string

// Arrays vs Sets vs Tuples
// Usar tuplas para colecciones específicas, que no cambiarán en estructura y cuyos 
// conceptos permanecerán con el mismo nombre/posición
let address = (house: 555, street: "Taylor Swift Avenue", city: "Nashville")
print(address)

// Usar Sets para colecciones que no se repiten o para validar si existe un valor de 
// forma rápida
let set = Set(["aardvark", "astronaut", "azalea"])
print(set)

// Usa arreglos para colecciones que pueden tener duplicados, donde la posición importa
let pythons = ["Eric", "Graham", "John", "Michael", "Terry", "Terry"]
print(pythons)

// Diccionarios
// Colecciones de clave valor, la clave es la posición de diccionario y accede al valor guardado
let heights = [
    "Taylor Swift": 1.78,
    "Ed Sheeran": 1.73
]
print(heights)
print(heights["Taylor Swift"])
// Los valores se separan con coma y las claves se separan de su valor por :

// Diccionarios con valores por defecto
let favoriteIceCream = [
    "Paul": "Chocolate",
    "Sophie": "Vanilla"
]
// Valor asignado
print(favoriteIceCream["Paul"])
// valor no asignado
print(favoriteIceCream["Charlotte"])
// valor no asignado con valor por defecto
print(favoriteIceCream["Charlotte", default: "Unknown"])

// Crear colecciones vacias
// Es posible crear colecciones (arreglos, diccionarios  y sets) solo si se especifica de que tipo 
// de valor serán

// Diccionario 
var teams = [String: String]()
print(teams)
teams["Paul"] = "Red"
print(teams["Paul"])

// Array
var results = [Int]()
print(results)
results.append(1)
print(results)

// SET
var words = Set<String>()
print(words)
var numbers = Set<Int>()
print(numbers)
// Esta estructura también se usa para diccionarios y arreglos
var scores = Dictionary<String, Int>()
print(scores)
var results2 = Array<Int>()
print(results2)

// Enumerales
// Definen un tipo que puede tomar diferentes valores. Evita duplicidades
enum Result {
    case success
    case failure
}
let result4 = Result.failure
print(result4)
// Enumerales con valores asociados
enum Activity {
    case bored
    case running
    case talking
    case singing
} // enum simple
enum Activity2 {
    case bored
    case running(destination: String)
    case talking(topic: String)
    case singing(volume: Int)
} // enums asociados
let talking = Activity2.talking(topic: "football")
print(talking)

// Enum raw value
// Para creación de enums dinámicos(como instancias)
enum Planet: Int {
    case mercury
    case venus
    case earth
    case mars
}
let earth = Planet(rawValue: 2)
print(earth)

// asignar al crear
enum Planet2: Int {
    case mercury = 1
    case venus
    case earth
    case mars
}
let earth2 = Planet2(rawValue:1)
print(earth2)

//  ----

// LOOPS
// Loops
let count = 1...10
for number in count {
    print("Number is \(number)")
}
let albums = ["Red", "1989", "Reputation"]
// Con arreglos
for album in albums {
    print("\(album) is on Apple Music")
}

// No es necesario crear variables para los contadores
print("Players gonna ")

for _ in 1...5 {
    print("play")
}

// Ciclos while
var number = 1

while number <= 20 {
    print(number)
    number += 1
}

print("Ready or not, here I come!")

// Ciclos repetitivos
var number2 = 1

repeat {
    print(number2)
    number2 += 1
} while number2 <= 20

print("Ready or not, here I come!")
// No entra en la condicion
while false {
    print("This is false")
}
// Entra en la condicion
repeat {
    print("--This is false")
} while false

// Salir de un ciclo
var countDown = 10
while countDown >= 0 {
    print(countDown)

    if countDown == 4 {
        print("I'm bored. Let's go now!")
        break
    }

    countDown -= 1
}

// Salidas multiples de los ciclos
for i in 1...10 {
    for j in 1...10 {
        let product = i * j
        print ("\(i) * \(j) is \(product)")
    }
}

// usos de outerLoop
outerLoop: for i in 1...10 {
    for j in 1...10 {
        let product = i * j
        print ("\(i) * \(j) is \(product)")

        if product == 50 {
            print("It's a bullseye!")
            break outerLoop
        }
    }
}

// sin break
outerLoop: for i in 1...10 {
    for j in 1...10 {
        let product = i * j
        print ("\(i) * \(j) is \(product)")
    }
}

// Saltar conceptos
// usos de continue
for i in 1...10 {
    if i % 2 == 1 {
        continue
    }

    print(i)
}

// ciclos infinitos
/* 
var counter = 0

while true {
    print(" ")
    counter += 1

    if counter == 273 {
        break
    }
}
*/
// -----


// STRUCTS 
/* Estructuras
Son formas de crear nuestros propios tipos de datos, las estructuras se componen de 
constantes y variables(propiedades), así como de sus funciones(métodos)

*/
struct Sport {
    var name: String // stored property
}
// Para usarlas, se crean instancias de las estructuras
var tennis = Sport(name: "Tennis")
print(tennis.name)
// Se puede cambiar el valor de la propiedad
tennis.name = "Lawn tennis"
print(tennis.name)

// Computed properties
// Cambian de valor al correr cierto código
struct Sport2 {
    var name: String
    var isOlympicSport: Bool

    var olympicStatus: String {
        if isOlympicSport {
            return "\(name) is an Olympic sport"
        } else {
            return "\(name) is not an Olympic sport"
        }
    }
}

let chessBoxing = Sport2(name: "Chessboxing", isOlympicSport: false)
print(chessBoxing.olympicStatus)
let swimming = Sport2(name: "Swimming", isOlympicSport: true)
print(swimming.olympicStatus)


/*
Observadores de propiedad:
Permiten correr código antes o después de que cambie una propiedad
*/
struct Progress {
    var task: String
    var amount: Int
}
// Crear una intancia y cambiar los valores
var progress = Progress(task: "Loading data", amount: 0)
progress.amount = 30
progress.amount = 80
progress.amount = 100
print(progress.amount)
// La propiedad didSet observa por cambios en la propiedad indicada
struct Progress2 {
    var task: String
    var amount: Int {
        didSet {
            print("\(task) is now \(amount)% complete")
        }
    }
}
var progress2 = Progress2(task: "Loading data", amount: 0)
progress2.amount = 30
progress2.amount = 80
progress2.amount = 100

// Con willSet puedes tomar acciones antes de cambiar la propiedad

struct Progress3 {
    var task: String
    var amount: Int {
        willSet {
            print("\(task) is change to \(amount)% complete")
        }
    }
}
var progress3 = Progress3(task: "Loading data", amount: 0)
progress3.amount = 30
progress3.amount = 80
progress3.amount = 100


/*
métodos
Funciones que pueden usar las propiedades de la estructura
*/
struct City {
    var population: Int

    func collectTaxes() -> Int {
        return population * 1000
    }
}
let london = City(population: 9_000_000)
let myLondon = london.collectTaxes()
print(myLondon)
// Mutación de métodos
// Ayudan a indicar que un método mutara de valor una 
// propiedad de la estructura

struct Person {
    var name: String

    mutating func makeAnonymous() {
        name = "Anonymous"
    }
}

var person = Person(name: "Ed")
person.makeAnonymous()
print(person.name)

// Propiedades y métodos de strings
let string = "Do or do not, there is no try."
// Número de caracteres
print(string.count)
// Identifica si un substring esta contenido en:
print(string.hasPrefix("Do"))
// Convierte a mayusculas
print(string.uppercased())
// Crea un arreglo con las letras ordenadas
print(string.sorted())

// Propiedades y métodos de los arreglos
var toys = ["Woody"]
// Número de items:
print(toys.count)
// Agrega un elemento al final
toys.append("Buzz")
print(toys)
// Encuentra el indice de un elemento
toys.firstIndex(of: "Buzz")
print(toys.firstIndex(of: "Buzz"))
// ordena el arreglo
print(toys.sorted())
// remueve un elemento
toys.remove(at: 0)
print(toys)

// Inicializadores
// Indican si se quiere crear una estructura con un valor por defecto

// Sin inicializador
struct User {
    var username: String
}
var user = User(username: "twostraws")
print(user)

// con inicializador
struct User2 {
    var username: String

    init() {
        username = "Anonymous"
        print("Creating a new user!")
    }
}

var user2 = User2()
// no es necesario usar el keyword func para inicializadores, 
// pero es obligatorio que todos los valores tengan un valor antes
// de que finalice el inicializador
user2.username = "twostraws"
print(user2.username)

// Referencia al a instancia en curso
/*
Esta propiedad ayuda a referir a las propiedades que se
encuentran dentro de la estructura y se refieren a la instancia creada
Son muy utiles al distinguir entre propiedades (self) y parámetros 
*/
struct PersonSelf {
    var name: String

    init(name: String) {
        print("\(name) was born!")
        self.name = name
    }
}
var myPerson = PersonSelf(name: "Yocelin")
print(myPerson.name)

/*
Propiedades flojas xD
Ayudan a crear propiedades solo cuando es necesario
*/
struct FamilyTree {
    init() {
        print("Creating family tree!")
    }
}

struct PersonLazy {
    var name: String
    lazy  var familyTree = FamilyTree()

    init(name: String) {
        self.name = name
    }
}

var ed = PersonLazy(name: "Ed")
print(ed.familyTree)
/*
Propiedades estáticas y métodos
Cada estructura permite crear diferentes instancias de ella
*/
struct Student {
    var name: String

    init(name: String) {
        self.name = name
    }
}

let ed2 = Student(name: "Ed")
print(ed2.name)
let taylor = Student(name: "Taylor")
print(taylor.name)

// si se declaran propiedades o métodos como static tendrán el
// mismo valor para cada isntancia
struct StudentStatic {
    static var classSize = 0
    var name: String

    init(name: String) {
        self.name = name
        StudentStatic.classSize += 1
    }
}
let ed3 = StudentStatic(name: "Ed")
print(StudentStatic.classSize)

/*
Control de acceso
Restringe qué código puede usar propiedades y métodos
*/
struct PersonId {
    var id: String

    init(id: String) {
        self.id = id
    }
}

let edId = PersonId(id: "12345")
print(edId.id)
struct PersonPrivate {
    private var id: String

    init(id: String) {
        self.id = id
    }
}
/* No se puede:
let edIdPriv = PersonPrivate(id: "12345")
print(edIdPriv.id)
*/

struct PersonPrivateTrue {
    private var id: String

    init(id: String) {
        self.id = id
    }

    func identify() -> String {
        return "My social security number is \(id)"
    }
}

let edIdPriv2 = PersonPrivateTrue(id: "12345")
print(edIdPriv2.identify())

// ------

// CLASS
/*
CLASES:
Permiten crear tipos de datos con propiedades y métodos
Existen algunas diferencias entre las clases y las estructuras.
1. Las clases no tienen un inicializador (miembro), lo
cual implica que siempre se deben de crear inicializadores propios. 
*/
class Dog {
    var name: String
    var breed: String

    init(name: String, breed: String) {
        self.name = name
        self.breed = breed
    }
}
// Al crear una instancia de la clase, se ejecuta el inicializador
let poppy = Dog(name: "Poppy", breed: "Poodle")
print(poppy.name, poppy.breed)


/* Herencia de clases
2. Puedes crear una clase con base en una clase que ya existe,
la nueva clase hereda todas las propiedades y métodos de la clase
original y puede añadir nuevos.
A este comportamiento se le denomina herencia de clases o subclassing.
La clase original se denomina padre o clase super, mientras que a la nueva
se le denomina hija.
En el ejemplo, el inicializador, puede mandar llamar al inicializador
de la clase padre
*/
class Poodle: Dog {
    init(name: String) {
        super.init(name: name, breed: "Poodle")
    }
}
let perrito = Poodle(name: "Perrito")
print(perrito.name, perrito.breed)
// Por defecto, swift siempre llama la función super.init() 
// de la clase padre, dentro de la clase hija.

/*
Métodos de anulación
Son de utilidad para reemplazar métodos de una clase padre
por su propio método hijo, este proceso se le conoce como anulación
*/
class DogNoise {
    func makeNoise() {
        print("Woof!")
    }
}
// Su clase hija hereda su comportamiento
class PoodleNoise: DogNoise {
}

let poppyNoise = PoodleNoise()
poppyNoise.makeNoise()
/*
Agregar la keyword override func antes del método a sobreescribir
se realizará el proceso, si no se agrega el keyword y se intenta 
sobre escribir la función, resultará en un error
*/
class PoodleOverride: DogNoise {
    override func makeNoise() {
        print("Yip!")
    }
}
let poppyNoiseOverride = PoodleOverride()
poppyNoiseOverride.makeNoise()

/*
Clases finales
Es posible proteger una clase para que no tenga override añadiendo 
el keyword final al principio de la declaración
De est forma, se tendrá que usar la clase tal como esta escrita
*/
final class DogFinal {
    var name: String
    var breed: String

    init(name: String, breed: String) {
        self.name = name
        self.breed = breed
    }
}
let poppyFinal = DogFinal(name: "Patitas de coneja", breed: "Labarador")
print(poppyFinal.name, poppyFinal.breed)
/*
Copiando objetos
3. La tercer diferencia es como se copian las clases y estructuras
Las estructuras son diferentes (original y copias)
Las clases y sus copias apuntan (en dirección) al mismo lugar, si cambias una
todos lo harán
*/
class Singer {
    var name = "Taylor Swift"
}
// La insancia conserva el valor de la clase
var singer = Singer()
print(singer.name)
// Las copias nuevas apuntan a la misma dirección de memoria
var singerCopy = singer
singerCopy.name = "Justin Bieber"
print(singer.name)
/*
Desinicializadores
4. Las clases, a diferencia de las estructuras, tienen de inicializadores
Son códigos que pueden correr cuando una instancia de la clase se destruye
*/
class Person {
    var name = "John Doe"

    init() {
        print("\(name) is alive!")
    }

    func printGreeting() {
        print("Hello, I'm \(name)")
    }
    deinit {
        print("\(name) is no more!")
    }
}

for _ in 1...3 {
    let person = Person()
    person.printGreeting()
}
/*
Mutabilidad
5. Manejo de constantes: Las propiedades de las clases pueden cambiar
aunque la clase sea constante
*/
class SingerMutate {
    var name = "Taylor Swift"
}

let taylor = SingerMutate()
taylor.name = "Ed Sheeran"
print(taylor.name)
// Variables constantes
class SingerConst {
    let name = "Taylor Swift"
}
let taylor2 = SingerConst()
// Debe ser error: taylor2.name = "Ed Sheeran"
print(taylor2.name)
// -----
 
/* OPTIONALS
Manejo de perdida de información
Se usan para dar una respuesta cuando lo que se solicita 
no tiene valor
*/
var age: Int? = nil
age = 38
print(age)

/*
Deselvonviendo opcionales
Cuando una variable esta vacía en memoria, su valor en nil,
por lo que apesar de que este definido para tener cierto tipo de dato, no podrá acceder 
a los métodos definidos para él
El proceso de unwrapping,  es aquel que permite manejar estos casos para 
prevenir que el proceso se inseguro.
Uno de los métodos usados, es el uso de if let, en el que se crea la variable 
si existe, en caso contrario fallará
*/
var name: String? = nil
if let unwrapped = name {
    print("\(unwrapped.count) letters")
} else {
    print("Missing name.")
}
/*
La variable name será un string, si se cumple la condición de existencia, entrará 
dentro del unwrapped como un string regular, y podrá usar todas las propiedades de string
en caso contrario correrá el código del else 
*/
/*
Unwrapping con guarda
Otra alternativa, es el uso de guard let, el cual manejar las variables como opcionales
y si encuentra nil, saldra de la función, ciclo o condición que lo use
Con guard let, la variable sige siendo usable fuera de la condición
*/
func greet(_ name: String?) {
    guard let unwrapped = name else {
        print("You didn't provide a name!")
        return
    }

    print("Hello, \(unwrapped)!")
}
greet("Yocelin")
greet(nil)

/*
Unwrapping forzado
Cuando un valor puede o no existir, es util usar el unwrapping, cuando esto sucede y el valor que tomará la variable tendrá
un valor especifíco, es recomendable usar el unwrapping forzado. 
*/
let str = "5"
let num = Int(str)
// Escribiendo ! después de Int(str) aseguramos que siembre se haga la asignación si el valor de str es casteable //// como Int
let num2 = Int(str)!
/* Es necesario aclarar que si no es casteable, la app romperá, por lo que solo es recomendable usar este caso cuando se este seguro
que siempre se cumplirá la condición*/

/*
OPCIONALES IMPLICITOS CON UNWRAPPING
Este tipo de opcionales, pueden tener un valor o pueden ser nil, pero no necesitan ser desenvueltas para poder usarse, se crean al agregar 
un signo de ! después del tipo de dato y se les asigna el valor nil, dado esto, se comportan como si estuvieran desenvueltos sin necesidad de 
usar if let o guard let, pero si no tienen un valor, el código fallará*/


let age: Int! = nil

/*
NIL COALESCING
Son de ayuda para proporcionar un retorno a un valor con base en una comparación, deberá asignarse un valor por defecto
*/

func username(for id: Int) -> String? {
    if id == 1 {
        return "Taylor Swift"
    } else {
        return nil
    }
}
// Funcionalidad correcta
let user = username(for: 15) ?? "Anonymous"
print(user)
/*
Encadenamiento opcional
Cuando se hace una operación sobre varias variables, y alguna es opcional, es necesario añadirle el signo de ? para que si no 
existe, se ignore el resto de la linea y regrese nil, en caso contrario, se hara unwrapping y continuará el proceso
*/
let names = ["John", "Paul", "George", "Ringo"]
let beatle = names.first?.uppercased()
print(beatle)
let names2 = [nil, "Paul", "George", "Ringo"]
// NO corre: let beatle2 = names2.first?.uppercased()
// print(beatle2)

/*
Try opcional
*/
// Correr try catch
enum PasswordError: Error {
    case obvious
}

func checkPassword(_ password: String) throws -> Bool {
    if password == "password" {
        throw PasswordError.obvious
    }

    return true
}

do {
    try checkPassword("password")
    print("That password is good!")
} catch {
    print("You can't use that password.")
}
/*
Existen otras opciones ante el uso de do, try -> catch, una de ellas usa unwrapping y es el uso de try?, que hace uso de funciones que 
retornan un opcional, si la función resulta en un error, regresa nil como resultado, en caso contrario, regresa el valor opcional
*/
if let result = try? checkPassword("password") {
    print("Result was \(result)")
} else {
    print("D'oh.")
}
if let result2 = try? checkPassword("password2") {
    print("Result was \(result2)")
} else {
    print("D'oh.")
}
/*
Otra alternativa, el el uso de try!, que solo se usará cuando se sabe que la funcion resultará de forma positiva
*/
try! checkPassword("sekrit")
print("OK!")

/*
INICIALIZADORES QUE FALLAN  
Es posible hacer uso de opcionales para las funciones init de clases y estructuraas, donde en caso de fallar, inicializará las propiedades
como nil y en caso de existo, asignará un valor
*/
struct Person {
    var id: String

    init?(id: String) {
        if id.count == 9 {
            self.id = id
        } else {
            return nil
        }
    }
}
let abril =  Person(id: "123456789")
print(abril == nil) // Es falso, por que el id tiene la longitud adecuada
let abril2 =  Person(id: "1234")
print(abril2 == nil) // Es true por que la longitud es menor

/*Typecasiting
Hace Un retorno opcional dependiendo del tipo de si el tipo 
de dato por el que se pregunta, cumple la condiciòn
En el ejemplo, se tiene un arreglo de mascotas que contiene 
intancias de una clase (algunas son derivadas de la calse
original, y otras son derivadas de una clase hija) 
Este arreglo serà de clase Animals (por inferencia de tipo)
y se hecharà mano del typecasting para saber en cual de 
esos conceptos, se puede invocar el método makeNoise()
*/
class Animal { }
class Fish: Animal { }

class Dog: Animal {
    func makeNoise() {
        print("Woof!")
    }
}
let pets = [Fish(), Dog(), Fish(), Dog()]
for pet in pets {
    if let dog = pet as? Dog {
        dog.makeNoise()
    }
}

// -----
```
