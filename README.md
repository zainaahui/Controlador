[readme_del_controlador_para_juego_web.md](https://github.com/user-attachments/files/34104427/readme_del_controlador_para_juego_web.md)
# Controlador Físico Interactivo para Videojuegos Web 🕹️

Este repositorio documenta el proceso de diseño, modelado 3D, electrónica y ensamblaje de un controlador físico personalizado creado con Arduino, diseñado específicamente para interactuar y controlar un videojuego alojado en una página web.

## 📋 Descripción del Proyecto

El objetivo de este proyecto es tender un puente entre el hardware físico y el software web. Mediante el uso de un microcontrolador Arduino Uno, componentes de entrada analógicos y digitales (un potenciómetro deslizante y un pulsador tipo arcade), y una carcasa diseñada a medida, este controlador permite enviar comandos interactivos en tiempo real a una aplicación web.

## 🛠️ Componentes y Materiales

### 1. Electrónica y Hardware

* **Microcontrolador:** Arduino Uno R3 (con cable USB para conexión y comunicación serial).
* **Entrada Analógica:** Potenciómetro deslizante para controles de posición o navegación lineal.
* **Entrada Digital:** Pulsador / botón tipo arcade (con su respectivo switch microswitch) para acciones principales o saltos.
* **Conexión y Prototipado:** Placa perforada (*perfboard*) y cables de conexión (*jumpers*).

### 2. Diseño y Fabricación de la Carcasa (Rhino 3D)

* **Software de Modelado:** Rhinoceros 3D (para el diseño CAD de la caja contenedora y el panel de control superior).
* **Estrategia de Ensamblaje:** Estructura tipo caja encajable con pestañas de ajuste y una cubierta superior adaptada para los componentes.

---

## ⚙️ Proceso de Creación y Desarrollo

### Fase 1: Diseño 3D en Rhinoceros
En esta etapa se planificó la volumetría y distribución espacial de todos los elementos del controlador mediante modelado CAD.

![Diseño CAD y planimetría en Rhino](IMG_3639.jpg)
*Vistas técnicas en Rhino mostrando el diseño de las caras de la caja, el panel superior con la ranura para el slider y el espacio para el botón arcade.*

![Modelo 3D ensamblado](Captura%20de%20pantalla%202026-10-28%20192742.png)
*Renderizado preliminar del modelo 3D de la carcasa abierta y sus piezas listas para el encaje.*

---

### Fase 2: Prototipado Electrónico y Cableado
Se realizaron las conexiones iniciales para verificar la lectura de señales analógicas y digitales a través de los pines del Arduino Uno.

![Conexiones iniciales con Arduino Uno](IMG_3637.jpg)
*Prueba de cableado inicial conectando directamente el potenciómetro deslizante y el pulsador arcade al Arduino Uno.*

---

### Fase 3: Soldadura y Montaje en Placa Perforada
Una vez validado el circuito, las conexiones se trasladaron a una placa perforada para asegurar mayor estabilidad y orden en el circuito interno.

![Ensamblaje en placa perforada](IMG_3638.jpg)
*Distribución definitiva de los componentes electrónicos soldados sobre la placa perforada.*

---

### Fase 4: Integración con la Página Web (Próximamente)
* Configuración del puerto serial mediante JavaScript / Web APIs para leer los valores físicos en tiempo real.
* Mapeo de las entradas del controlador a las acciones del videojuego en línea.

## 📸 Galería del Proceso

> *Nota: Las fotografías finales del ensamblaje definitivo del controlador integrado dentro de la carcasa impresa/cortada se añadirán próximamente.*

## 🚀 Próximos Pasos

1. Corte y ensamblaje de la carcasa física basándose en los modelos 3D de Rhino.
2. Integración final de la electrónica dentro de la caja.
3. Pruebas de jugabilidad conectando el controlador físico con el juego web.
