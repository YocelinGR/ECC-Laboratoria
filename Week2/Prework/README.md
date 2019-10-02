# Preguntas de Prework

01. Entra a https://www.hackingwithswift.com/sixty y en la página online.swiftplayground.run haz las siguientes secciones:

02. i. Complex Types

   ii. Operators and conditions
   iii. Looping
   iv. Functions
   v. Structs

``` swift
    import Foundation
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
// valor. Las tuplas:
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
// Usar tuplas para colecciones espefificas, que no cambiaran en estructura y cuyos 
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

// asinar al cre<r
enum Planet2: Int {
    case mercury = 1
    case venus
    case earth
    case mars
}
let earth2 = Planet2(rawValue:1)
print(earth2)

// Operadores y condicionales
// Operadores aritmèticos
let firstScore = 12
let secondScore = 4
// Adiciòn y substracciòn:
let total = firstScore + secondScore
let difference = firstScore - secondScore
print(total)
print(difference)
// Multiplicaciòm y divisiòn
let product = firstScore * secondScore
let divided = firstScore / secondScore
print(product)
print(divided)
// Remainder
let remainder = 13 % secondScore
print(remainder)

// sobrecarga del operador
// Capacidad de usar un operador con varios tipos de datos
// Concatenacion
let meaningOfLife = 42
let doubleMeaning = 42 + 42
print(doubleMeaning)

let fakers = "Fakers gonna "
let action = fakers + "fake"
print(action)

let firstHalf = ["John", "Paul"]
let secondHalf = ["George", "Ringo"]
let beatles = firstHalf + secondHalf
print(beatles)

// Operadores de asignaciòn compuesta
// Combinan operadores con asignaciòn
var score = 95
score -= 5
print(score)

var quote = "The rain in Spain falls mainly on the "
quote += "Spaniards"
print(quote)

// Operadores de comparación
let first = 6
let second = 4
print(first == second)
print(first != second)
print(first < second)
print(first >= second)
print("Taylor" <= "Swift")

// Condiciones
let firstCard = 11
let secondCard = 10
// If
if firstCard + secondCard == 21 {
    print("Blackjack!")
}

// If - else
if firstCard + secondCard == 21 {
    print("Blackjack!")
} else {
    print("Regular cards")
}
// else if
if firstCard + secondCard == 2 {
    print("Aces – lucky!")
} else if firstCard + secondCard == 21 {
    print("Blackjack!")
} else {
    print("Regular cards")
}
// AND
let age1 = 12
let age2 = 21

if age1 > 18 && age2 > 18 {
    print("Both are over 18")
}

// OR
if age1 > 18 || age2 > 18 {
    print("One of them is over 18")
}
// Operador termanio
// Evalua el primer valor, regresa el segundo si la condicion es verdadera 
// y regresa el tercer valor si es falsa
let firstCard2 = 11
let secondCard2 = 10
print(firstCard2 == secondCard2 ? "Cards are the same" : "Cards are different")

// Es lo mismo que:
if firstCard2 == secondCard2 {
    print("Cards are the same")
} else {
    print("Cards are different")
}
// Switch
let weather = "sunny"
switch weather {
case "rain":
    print("Bring an umbrella")
case "snow":
    print("Wrap up warm")
case "sunny":
    print("Wear sunscreen")
default:
    print("Enjoy your day!")
}
// Usar fallthrough si se deseaque un caso continue en el siguiente
switch weather {
case "rain":
    print("Bring an umbrella")
case "snow":
    print("Wrap up warm")
case "sunny":
    print("Wear sunscreen")
    fallthrough
default:
    print("Enjoy your day!")
}

// Operadores de rangos
// ..< crea rangos y excluye el valor final
// ... crea rango e incluye el valor final
let score2 = 85

switch score2 {
case 0..<50:
    print("You failed badly.")
case 50..<85:
    print("You did OK.")
default:
    print("You did great!")
}

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

```

03. Entra a https://developer.apple.com/design/human-interface-guidelines/ios/overview/themes/ y contesta lo siguiente:

4.

    i. Enlista y describe los temas principales de diseño

    

    Para que una aplicación sobresalga, es necesario que la calidad y funcionalidad de la misma sean buenos y que además el diseño sea agradable e intuitivo.

     **Claridad**
     Todas las vistas tienen texto legible y los icónos y otros recursos visuales son de calidad. La funcionalidad de la aplicación se apoya del diseño y lo motiva.

     Hacer uso de detalles pequeños como el espacio, el color, las fuentes, graficos y elementos de la interfaz ayudan a resaltar de forma conveniente las interacciones que se espera que tenga el usario dentro de la aplicación.

     **Deferencia**
     Una interfaz intuitiva ayuda a entender como interactuar con ella, aún si nunca antes se ha tenido contacto con algo así, de esta manera, la interacción será fluida y sin dificultades.
     Una pantalla sin distracciones (con traslucidez y desenfoque) suele ser más sugerente que una vista cuyo contenido opupa todo el espacio.
     El minimo uso de marcos, degradasos y sombras hace que la interfaz sea clara y airada. Esto da protagonismo al contenido.

     **Profundidad**
     El uso de capas y el movimiento realista dan jerarquía, vitalidad y facilitan la comprensión.
     Cuando las interacciones son faciles de usar y de detectar, es posible acceder a la funcionalidad y el contenido adicional sin perder contexto.
     Las transiciones dan sensacion de profundidad/avance a medida que se navega por el contenido.

    ii. Enlista y describe los principios de diseño

    Los principios de diseño ayudan a maximisar el impacto y el alcance de la aplicación.

     **Integridad Estetica**
     Que tanto se integran la apariencia y el comportamiento con la funcionalidad. Que tanto la apariencia e interacciónes fomentan que se lleve a cabo el proposito de la aplicación.

     **Consistencia**
     Una aplicación consistente usa estándares y paradigmas por medio del uso elemetos de interfaz que pertenencen a un mismo sistema (icónos, estilos de texto, terminología uniforme). La aplicación incorpora características en la forma en que las personas lo esperan.
     *predecible* y *estandarizado*

     **Manipulación directa**
     La manipulación directa del contenido en la pantalla, engancha a las personas y facilita el entendimiento.
     La manipulación directa se logra cuando los susarios rotan el dispositivo o usan gestos para afectar el contenido en la pantalla y obtienen resultados inmediatos y visbles de sus acciones.

     **Retroalimentación**
     La retroalimentación es útil para mantener informada a los usuarios por medio del reconocimiento de las acciones del usuario. 
     En aplicaciones de iOS, proveen retroalimentación perceptible en respuesta a _cada accion_ del usuario.
     Los elementos interactivos se resaltan al tacto, los indicadores de progreso comunican el estado de las operaciones de larga duración, aspi como mas animaciones y sonidos ayudan a aclarar los resultados de las acciones. 

     **Metáforas**
     Las personas aprenden más rápido cuando los objetos y acciones virtuale se asemejan a experiencias familiares (reales o digitales).
     Algunos ejemplos son: la movilización entre vistas para descrubrir contenido, alterar interruptores o controles que se deslizan, desplazarse entre selectores e incluso nevegar entre paginas como si fuesen un libro. 

     **Control del usuario**
     La toma de decisiones debe de ser manejada por los usuarios, donde las aplicaciones deberían solo sugerir el curso de las acciones o mostrar las consecuencias de determinadas acciones. 
     Una buena app equilibra bien habilitar las acciones de los usuarios y evitar resultados no deseados. 
     Se puede lograr que los usuarios sientan que tienen el control manteniendo elementos interactivos familiares y predecibles, así como permitir que las acciones destructivas se puedan confirmar y cancelar (incluso si estan en marcha).

    iii. Dentro de la sección de User Interaction, describe lo siguiente:

    iv.

        a. Authentication/ Autenticación
            La autenticación solo debe usarse si se aporta valor para la aplicación, como por ejemplo, personalización, acceder a funciones adicionales, comprar contenido o sincronizar información. La autenticación con Inicio de sesión de Apple es simple y segura, además ofrece un inicio de sessión consistente y comoda.
            Alternativas adicionales a la autenticación con Apple:
            
            **Autollenado de Password**: Genera y llena el campo de passwordy códigos de seguridad.
            **Permitir estar autenticado por largos tiempos: Asegura que la interacción con la aplicación y la realización exitosa de acciones se efectue de forma adecuada.
            **Explicar los beneficios de la autenticación y como obtener una cuenta: Es importante consderar que no todos los usuarios no tendran una cuenta creada.
            **Maximiza la entrada de información mostrando teclados apropiados**: Habilita todas las herramientas necesarias para el usuario.
            **No usar el termino PassCode**: este esta reservado para desbloquear un dispositivo iOS y autenticar con Apple Pay cuando los biometricos no funcionan.

            _ FaceID y TouchID_
            Usar lo menos posible ya que no todos los usuarios pueden tener habilitada esta funcionalidad en su dispositivo.
            Consejos para hacer la autenticación más intuitiva:

            * Presentar una forma simple de autenticación (da la ventaja de no tener que escoger una)
            * Inicia la autenticación solo como respuesta a la interacción del usuario.
            * Usa identificadores para los metodos de autenticación
            * Usa métodos de autenticación precisos (habilita los métodos dependiendo de las capacidades de los dispositivos)
            * Evita ofrecer configuración para optar por autenticación biométrica(si esta habilidada en el sistema, asuma que el usuario quiere usarla, en caso contrario no sugerir para evitar confusiones de que si usa y que no esa forma de autenticación)
            * No usar iconos para identificar las características de autenticación del sistema(el usuario puede asumir que ciertas formas de autenticación con las que esta familiarizado esten habilitadas cuando esto no es cierto)

        b. Data Entry / Entradas de Datos
            Las entradas de datos deben de ser minimas para obtener resultados, o el proceso serà tedioso para el usuario.
            Algunas recomendaciones para hacer las interacciones con datos más comodas son:

                * Presenta opciones: Hace la información más eficiente.
                * Obten información del sistema lo más posible
                * Provee de valores por defecto: Proveer entradas de datos con los valores más comunes facilita la toma de deciciones y hace más rápio el proceso.
                * Permitir avanzar solo con los valores requeridos: Habilidar los elementos (botones, etc) cuando esto suceda.
                * Validación dinámica de campos: Validar antes de pasar a otro campo
                * Uso de valores requeridos solo cuando sea necesario
                * Facil navegación entre campos: Facilita el ordenamiento y la selección
                * Muestre el proposito del campo

        c. Gestures / Gestos
            Los gestos permiten tener una sensación de manipulación directa entre los objetos en la pantalla y los gestos en la pantalla.
            Consejos:

                - Usa gestos comunes para acciones comunes, considerar la posiblilidad de gestos personalizados solo si aplica para la aplicación

                - Evita el uso de gestos standar para acciones no estandar

                - Evite el uso de los gestos a los costados de la pantalla: evite que el usuario ingrese a las acciones del sistema.

                - Ofrezca gestos de acceso para complementar acciones

                - Usa gestos de multi dedo 

                - Gestos standar:
                    * Tap: Activa un control o seleccióna un objeto
                    * Drag: Mueve un elemento
                    * Flick: Hace scroll horizontal
                    * Swipe: Vuelve a la pantalla anterior o revela vistas ocultas, cuando se hace con cuetro dedos, navega entre aplicaciones.
                    * Doble tap: Hace zoom y centra la imagen
                    * Pellizco. Se acerca cuando se pellizca hacia afuera, se aleja cuando se pellizca hacia adentro.
                    * Toca y sostiene: En editores de texto, posiciona el cursor, en vistas reordena artículos
                    * Agitar: Deshacer o rehacer
                    * Totate: Rota una imagen o vista.

    v. Dentro de la sección de Visual Design, describe lo siguiente:

    vi.

        a. Adaptability and Layout
            Ser adaptable y responsivo en diferentes dispositivos, tamaño de pantallas y orientaciones.

            - Auto Layout: Herramienta que define reglas (constraints) que gobiernan el contenido de la app.

            Cambia los layouts de acuerdo a constraints especificos cuando variaciones conocidas (traits) sin detectadas. Es posibla adaptar:

                * Tamaños de pantalla, resoluciones y color
                * Orientación de dispositivos
                * Vista dividida
                * Modo multitare
                * Modo de escritura - cambios de tamaño del texto
                * Funciones de internacionalización (dirección, fecha y hora)
                * Funciones del sistema habilitadas (Touch 3d)
            - Guias de layout y área segura
                * Definen margenes que ayudan al posicionamiento, alineacion y espaciado. El sistema incluye guías de diseñoque facilitan la aplicación de márgenes estándar al rededor del conenido y restringen el espacio ocupado por el texto.
                * El uso de UIKit es consistente con las guias de layout
                * Las clases son variaciones (traits) que se asignan a las áreas de contenido con base en su tamaño. El sistema define tamaño regular (espacio expansivo) y compacto (espacio restringido) que describen el largo y ancho de la vista. Los tamaños se pueden combinar:
                    - Ancho regular, altura regular
                    - Ancho compacto, altura compacta
                    - Ancho regular, altura compacta
                    - Ancho compacto, altura regular
                * Clases de tamaño de dispositivo: Las combinaciones anteriores si definen para diferentes dispositivos en modo orizontal y vertical
                * Clases de tamaño multitarea: se aplica para el iPad y aplican para la division de pantalla.
            - Considerraciones generales de layout:
                * Asegura que el contenido primario es claro y con tamaño por defecto
                * Mantener apariencia general de forma consistente a lo largo de la aplicación
                * Usar peso visual y equilibro para transmitir importancia
                * Usa alineamiento para fácil escaneo y comunicar organización y herencia. Mantener al usuario enfocado y que puede identificar los grupos de contenido.
                * Dar soporte para uso con orientación horizontal y vertical
                * Dar soporte para cambios de tamaño de texto: Hacer uso del layout para ajustar la tipografía.
                * Provee de aplias áreas para elementos interactivos: 44pt por 44pt para todos los controles.
                * Obtener vistas de la aplicación en varios dispositivos y orientaciones 
                * Aplicar márgenes de legibilidad para mostrar texto en dispositivos más grandes: Mantiene lineas de texto cortas para su fácil lectura
            - Adaptar los cambios de contexto
                * Mantener la prioridad en el contenido actual durante cambios de contexto
                * Evitar cambios de diseño: Mantener experiencia comparable en todos los contextos (girar, tamaños)
                * Si es esencial que la aplicación se ejecute en una sola orientación, admitir ambas variantes
                * Customiza la respuesta de la aplicacion para recordar de acorde al contexto: reajustar menus, etc
                * Asegurarse que la aplicación funciona en iPad y iPhone
                * Considere el aspect ratio para diferentes dispositivos cuando se rehusaran ilustraciones
            - Diseñar experiencias full-screen
                * Extender elementos visuales para rellenar la pantalla.
                * Evitar colocar controles interactivos en la parte inferior en las esquinas: evite usar gestos del sistema, además son áreas difíciles de alcanzar.
                *  Insertar contenido esencial para evitar recortes: En general, el contenido debe estar centrado y simétricamente insertado para que se vea bien en cualquier orientación, es recomendable usar elementos de interfaz estándar, cumplir con las guías de diseño y áreas segura definidas por el UIKit
                * Considerar la altura de la barra de estado para diferentes dispositivos y funcionalidades como segundo plano.
                * Permitir la ocultación automática del indicador para acceder a la pantalla de inicio con moderación. Este comportamiento debe estar habilitado solo para experiencias de visualización pasiva como reproducir videos o presentaciones de fotos.

        b. Branding
        Las buenas aplicaciones expresan identidad de marca a través de fuentes, color y decisiones de imagen, suficientes para dar contexto, pero que no distraigan.

            * Incorporar una marca refinada y discreta
            * La marca no interfiere con el diseño de la aplicación: hacer que se sienta como app iOS, que sea intuitiva y que se centre en el contenido.
            * Considerar formas menos intrusivas de implementar la marca, como usar un esquema de color personalizado o una fuente, o personalizar sutilmente el fondo.
            * Evitar mostrar un logotipo en toda la aplicación, a menos que sea necesario

        c. Color

            * Usar el color juiciosamente para la comunicación. El poder del color para llamar la atención sobre información importante aumenta cuando se usa con moderación.
            * Usar colores complementarios en toda su aplicación.
            * Usa una paleta de color limitada que coordine con tu logo.
            * Considera elegir un color para indicar interactividad en la app
            * Provee dos versiones de color para que se ajusten al modo claro y obscuro de la app
            * Evita usar el mismo color para elementos en modo interactivo y el no interactivo
            * Considerar cómo las ilustraciones y la translucidez afectan los colores

            Realiza test de color de tu esquema bajo diferentes variaciones de luz

            * Considera como la pantalla True Tone afecta el color
            * Considera como el uso de color es percibido en otras culturas y paises
            * Evita el uso de colores que pueden hacer dificil percibir el contenido de la app
            * Sistema de color / sistema dinàmico
                * Usa colores primarios para la vista general
                * Usa colores secundarios para agrupar contenido o elementos dentro de la vista general
                * Usa colores terciarios para agrupar contenido o elementos dentro de los elementos secundarios
                * Colores definidos:
                    - Label -> class var label: UIColor { get }
                    - Secondary Label -> class var secondaryLabel: UIColor { get }
                    - Tertiary Label -> class var tertiaryLabel: UIColor { get }
                    - Quaternary Label -> class var quaternaryLabel: UIColor { get }
                    - Placeholder text -> class var placeholderText: UIColor { get }
                    - Separator: (permite que el contenido subyacente sea visible) -> class var separator: UIColor { get }
                    - Opaque separator: (no permite que el contenido subyacente sea visible)
                    - Link -> class var link: UIColor { get }
                * Manejo del color: 
                    - Aplicar colores de perfil a tus imagenes
                    - Usar un color amplio para mejorar la experiencia visual 

    vii. Dentro de la sección de _Controls_, describe lo siguiente:
    viii.

        a. Buttons:
           Los botones inician acciones especificas, es posible que tengan un fondo, titulo o un icono.  
           * Sistema de botones
            Generalmente aparecen en las barras de navegación y en las barras de herramientas, pero es posible usarlas en cualquier sitio. 
            Consejos para el uso de botones:

                * Usa verbos en sus titulos que expresen la acción que sucdderá si entra en modo interactivo
                * Escriba con mayúsculas cada palabra, excepto los artículos, las conjunciones de coordinación y las preposiciones de menos de cuatro letras.   * Manten los titulos cortos
                * Considera añadir un borde o fondo solo si es necesario  
                * Botones de dibulgación de detalles: Estos botones abren una vista (generalmente model) que contiene información adicional, se usan comúnmente en tablas para acceder ainformación sobre filas específicas. 
                * Usa los botones de dibulgación de detalles de forma adecuada en las tablas: no usar si se desea que al tocar toda la fila se puede ver el detalle de la misma.  
                * Botones de inofmración:  revelan detalles de configuración sobre una app.
                * Añade botones de agregar un nuevo elemento y habilite el teclado para estas nuevas entradas. 

        b. Labels 
            Describen un elemento de la enterfaz o proporcionan un mensaje corto. Pueden mostrar cualquier cantidad de texto estático, pero es mejor que sean cortos.    
            Es importante _mantener las etiquetas legibles_. Es recomentable usar el *Escritura dinámica* para mantener legible el texto, es recomendable probar estas opciones con el modo de accesibilidad habilitado. 

05. Enlista tus 10 apps favoritas
    - FrontEnd Masters: Nunca se traba, permite ver contenido offline, es muy legible y es fácil de navegar en ella, los icónos siempre se ven bien, el nivel de sonido siempre es suficiente, pero no excesivo. 
    - YouToBe: El buscador es muy bueno, puedes encontrar casi cualquier cosa 
    - YoutoBe Music: En la versión de paga puedes descargar tu musica o dejar que la app prediga que musica quieres escuchar offline según tus preferencias, el modo obscuro es muy comodo para la vista.
    - Slack: Todo lo que esta en la versión de escriorio esta en la versión mobil, puedes modificar las notificaciones, el diseño es muy bonito y muy intuitivo
    - Shazam: La interfaz es muy colorida, pero no distrae, si diseño es novedoso
06. Enlista y describe los cuatro pilares de la programación orientada a objetos
    - Abstracción: oculta la información que no se necesita saber para llevar a cabo una acción. Cada objeto solo expondrá un mecanismo de *alto nivel* para usarla. 
    - Encapsulación: La relación entre la información y las funciones que la manipulan para mantener la información a salvo, las funciones no afectan lo que hay en elexterior, esto los hace mantenibles y permite el cambio de forma fácil. Los estados (privados) y responsabilidades de cada clase estan definidas. Cada clase es discreta y autocontenida. Es posible acceder unicamente a una lista de funciones públicas desde el exterior (métodos), en algunas ocasiones, estas funciones pueden cambiar el estado interno, pero no lo haran de forma directa, si no por medio de acciones. 

    Ocultar el estado interno y requerir que toda la interacción se realice a través de los métodos de un objeto.

    - Herencia: Nuevos objetos pueden tomar propiedades de objetos que ya existen. Hay herencia de varios tipos:
        - Herencia simple: la clase hija, hereda el comportamiento de la clase padre y puede usar parámetros y funciones definidad antes.
        - Herencia multi nivel: La herencia se ejecuta en varios niveles. El hijo hereda el comportamiento del padre, quien a su vez ha heredado de una clase abuela. 
        - Herencia multiple: la herencia se puede tomar de varios padres. 
        - Herencia jerárquica: un padre puede tener varios hijos. 

    Nos ayudan a rehusar cosas. Los hijos rehusan todos los campos y métodos de los padres e implementan sus propios valores. 

    - Polimorfismo: capacidad de redefinir mètodos de otras clases,es decir, un objeto, puede comportarse de formas distintas. 
07. Dentro del paradigma de programación orientada a objetos:

8.

    i.¿Qué es un objeto? Es la unidad bàsica de la programaciòn orientada a objetos, se definen de un estado (representado por campos) y un comportamiento (representado por mètodos). Algunos de los beneficios del uso de objetos son:

        - Modularidad: el código fuente se puede cambiar sin afectar otros objetos
        - Ocultar información: Solo se interactua con los métodos del objeto, los detalles quedan ocualtos
        - Reutilización de código
        - Facilidad de conexión y depuración: es posible reemplazar objetos completos sin afectar el programa completo. Son instancias de las clases (entidad de trabajo)

    ii.¿Qué es una clase? Es una estructura (de datos) / tipo de datos que define las propiedades y el conjunto de instrucciones para construir un tipo específico de objetos, las clases tienen una sola responsabilidad.
    iii.¿Qué es un método? Todos los comportamients que puede tener una clase, son funciones que son parte de una clase
    iv.¿Qué es una propiedad? son campos de los objetos /clases que proporciona un mecanismo flexible para leer, escribir o calcular el valor de un campo privado, se usan para denotar una característica particular, abarcan los atributos como sus relaciones con otras clases. 

09. Investiga y describe la arquitectura de diseño MVC

    Es un patrón de arquitectura de software que usa 3 componentes: vistas, modelos y controladores, separando la lógica de la aplicación de la lógica de la vista en una aplicación. El usuario solicita al controlador quien comunica en ambos sentidos los datos con el modelo, asu vez el controlador envia los datos a la vista para que se actualice y responda visualmente al usuario. 
    La principal utilidad de este modelo es mantener las partes de nuestra aplicación separadas por su responsabilidad. 

        - El modelo se encarga de los datos, actualizaciones, consultas y búsquedas
        - El controlador se encarga de la lógica de la aplicación, recibe las ordenes, solicita datos al modelo y los comunica a la vista
        - La vista presentan los datos y toda la interfaz gráfica. 
10. ¿Qué es un ViewController?

    Es un gestor entre la aplicación y la pantalla, controla las vistas que posee de acuerdo a la lógica progrmada, administra un grupo de objetos de vista conoce el funcionamiento de la aplicación. 
    Un controlador de vista gestiona un conjunto de vistas y ayuda a crear la interfaz de usuario de la aplicación. Se coordina con objetos modelo y otros objetos controladores. 
    Un ViewController puede manejar una vista con varias subvistas

11. ¿Qué es un Storyboard?

    Elementos que nos permiten crear interfaces y manejar el flujo de navegación completo de la app, además permiten crear una app multivista sin usar una gran cantidad de código (todo desde un mismo archivo). 
    Los segues (transiciones) se pueden realizar de manera fácil enre diversas escenas

12. ¿Qué es un IBAction?

    Son funciones que permite conectar las acciones que tendra un elemento de la vista con el storyboard 

13. ¿Qué es un IBOutlet?

    Son variables que tomarán un valor cuano un NIB (Objeto Constructor de Interfaz)  se carga

14. ¿Qué es la notación CamelCase y cuáles son sus tipos? 

    Es una convención para el nombraiento de variables y funciones en programación en donde la primer letrea de cada palabra de una palabra compuesta vaen mayúsculas.
    Tipos:

        - lowerCamelCase
        - UpperCamelCase
15. ¿Conoces otro tipo de notación?
    - Sneak Case: my_var
    - Hungarian notation: isActive()
16. ¿Qué es un IDE y cuáles son sus elementos principales?

    _Entorno de Desarrollo integrado_ es un ambiente todo en uno que brinda distintas herramientas para escribir un programa, permiten realizar actividades comunes relacioadas al desarollo desde una misma aplicación: edición del código, creación de ejecutables, depuración, etc. 

    - Edición de código fuente
        - Resaltadode sintaxis
        - Autocompletado
    - Ejecutables de construcción
    - Depuración 
    - Control de versiones

## Notas:

* Interfaz esencial

    UIKit: framework programable quedefine elementos de interfaz comunes, con ello permitiendo generar aplicaciones con apariencia consistente a lo largo del sistema que también sean customizables con elementos flexibles y familiares. Lois elementos de un UIKit se dividen en tres categorias principales:

        * Barras: Permiten ubicarse en la aplicación y ofrecen navegación, pueden contener botones o otros elementos que permitan inicial acciones y comunicar información
        * Vistas: Contienen la información principal que se debe ver en la aplicación, como texto, graficos, animaciones y elementos interactivos. Las vistas pueden habilitar comportamientos como scroll, inserción, eliminación y gestión. 
        * Controles: Inician acciones y transmiten información. Algunos ejemplos son: botones, switches, campos de texto e indicadores de progreso. 

    Los UIKit también definen la funcionalidad que la aplicación puede adoptar

