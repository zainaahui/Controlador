Controlador Físico Interactivo para Videojuegos Web 🕹️

Este repositorio documenta el proceso de diseño, modelado 3D, electrónica y ensamblaje de un controlador físico personalizado creado con Arduino, diseñado específicamente para interactuar y controlar un videojuego alojado en una página web.

📋 Descripción del Proyecto

El objetivo de este proyecto es tender un puente entre el hardware físico y el software web. Mediante el uso de un microcontrolador Arduino Uno, componentes de entrada analógicos y digitales (un potenciómetro deslizante y un pulsador tipo arcade), y una carcasa diseñada a medida, este controlador permite enviar comandos interactivos en tiempo real a una aplicación web.

🛠️ Componentes y Materiales

1. Electrónica y Hardware

Microcontrolador: Arduino Uno R3 con cable USB.

Entrada Analógica: Potenciómetro deslizante.

Entrada Digital: Pulsador o botón tipo arcade con microswitch.

Conexión: Placa perforada (perfboard) y cables de conexión (jumpers).

2. Diseño y Fabricación de la Carcasa

Software: Rhinoceros 3D para el diseño CAD de la caja y la tapa superior con orificios precisos.

⚙️ Proceso de Creación y Desarrollo

Fase 1: Diseño 3D en Rhinoceros

En esta etapa inicial se planificó la volumetría de la caja contenedora, las pestañas de encaje y las aberturas específicas para el potenciómetro y el botón arcade.


Figura 1: Vistas técnicas de los planos y componentes en Rhinoceros 3D.


Figura 2: Vista isométrica del modelo 3D de la carcasa abierta y sus piezas listas para ensamblar.

Fase 2: Prototipado Electrónico y Cableado

Se realizaron las conexiones iniciales y pruebas de lectura en el protoboard / Arduino para asegurar el correcto funcionamiento del slider y el pulsador.


Figura 3: Conexión inicial de prueba entre los componentes y el Arduino Uno.

Fase 3: Soldadura y Montaje en Placa Perforada

Una vez validadas las señales, el circuito se trasladó a una placa perforada para compactar las conexiones y dotar al sistema de mayor robustez.


Figura 4: Distribución y soldadura definitiva sobre la placa perforada.

Fase 4: Ensamblaje Final y Pruebas con el Juego Web (Próximamente)

Nota: Las fotografías reales del montaje definitivo con todos los elementos integrados dentro de la carcasa cortada/impresa se añadirán en cuanto finalice el ensamblaje físico final.

[Insertar aquí la foto del controlador físico terminado y cerrado]

🚀 Próximos Pasos

Corte y ensamblaje físico de la carcasa según los planos de Rhino.

Integración final del circuito dentro de la caja.

Conexión y mapeo de eventos con el juego web mediante comunicación serial / Web APIs.
