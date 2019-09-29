# Preguntas de Prework

1. Entra a https://www.hackingwithswift.com/sixty y en la página online.swiftplayground.run haz las siguientes secciones:

2. i. Complex Types

   ii. Operators and conditions
   iii. Looping
   iv. Functions
   v. Structs

``` swift

```

3. Entra a https://developer.apple.com/design/human-interface-guidelines/ios/overview/themes/ y contesta lo siguiente:

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
    vii. Dentro de la sección de Controls, describe lo siguiente:

    viii.

        a. Buttons
        b. Labels
        c. Color

5. Enlista tus 10 apps favoritas

6. Enlista y describe los cuatro pilares de la programación orientada a objetos

7. Dentro del paradigma de programación orientada a objetos:

8. 
    i.¿Qué es un objeto?
    ii.¿Qué es una clase?
    iii.¿Qué es un método?
    iv.¿Qué es una propiedad?

9. Investiga y describe la arquitectura de diseño MVC

10. ¿Qué es un ViewController?

11. ¿Qué es un Storyboard?

12. ¿Qué es un IBAction?

13. ¿Qué es un IBOutlet?

14. ¿Qué es la notación CamelCase y cuáles son sus tipos? 

15. ¿Conoces otro tipo de notación?

16. ¿Qué es un IDE y cuáles son sus elementos principales?



## Notas:

* Interfaz esencial
    UIKit: framework programable quedefine elementos de interfaz comunes, con ello permitiendo generar aplicaciones con apariencia consistente a lo largo del sistema que también sean customizables con elementos flexibles y familiares. Lois elementos de un UIKit se dividen en tres categorias principales:
        * Barras: Permiten ubicarse en la aplicación y ofrecen navegación, pueden contener botones o otros elementos que permitan inicial acciones y comunicar información
        * Vistas: Contienen la información principal que se debe ver en la aplicación, como texto, graficos, animaciones y elementos interactivos. Las vistas pueden habilitar comportamientos como scroll, inserción, eliminación y gestión. 
        * Controles: Inician acciones y transmiten información. Algunos ejemplos son: botones, switches, campos de texto e indicadores de progreso. 
    Los UIKit también definen la funcionalidad que la aplicación puede adoptar
