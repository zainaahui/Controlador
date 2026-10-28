# 🎮 Controlador Físico Interactivo para Web Games

Controlador de hardware personalizado diseñado con **Arduino Uno**, un potenciómetro deslizante, un pulsador de arcade y un gabinete de MDF cortado a láser, pensado para interactuar con un juego alojado en una página web.

---

## 🛠️ 1. Componentes y Electrónica
En esta primera fase se realizó la selección de componentes y el cableado preliminar para verificar la lectura de señales analógicas y digitales.

* **Arduino Uno R3** como microcontrolador principal.
* **Potenciómetro deslizante** (control de eje lineal).
* **Pulsador de arcade** con microswitch (acción de disparo/salto).
* **Placa perforada (Perfboard)** para la consolidación de conexiones.

<div align="center">
  <img src="ruta/a/tu/carpeta/IMG_3637.jpg" width="45%" alt="Pruebas de cableado en protoboard/Arduino">
  <img src="ruta/a/tu/carpeta/IMG_3638.jpg" width="45%" alt="Soldadura y montaje en placa perforada">
</div>
![Circuito con Arduino Uno](assets/IMG_3637.jpg)
![Montaje en placa perforada](assets/IMG_3638.jpg)
![Modelado en Rhino 3D](assets/IMG_3639.jpg)
![Render del gabinete](assets/Captura%20de%20pantalla%202026-10-28%20192742.png)
---

## 📐 2. Diseño CAD 3D (Rhinoceros 8)
El gabinete fue modelado digitalmente considerando las tolerancias exactas para albergar el Arduino, el cableado y los elementos de interfaz superior (la ranura para el deslizador y el agujero para el botón de arcade).

* Modelado volumétrico de la caja con pestañas de unión tipo finger-joint.
* Distribución espacial superior para ergonomía del jugador.

<div align="center">
  <img src="ruta/a/tu/carpeta/IMG_3639.jpg" width="45%" alt="Proceso de diseño en Rhino 3D">
  <img src="ruta/a/tu/carpeta/Captura%20de%20pantalla%202026-10-28%20192742.png" width="45%" alt="Render de piezas despiezadas para corte láser">
</div>

---

## 🏗️ 3. Fabricación y Ensamblaje Final
*Corte láser de las piezas de MDF y ensamblaje de la estructura.*

> 📷 *(Espacio reservado para las fotos del montaje final de la caja cortada a láser)*

---

## 💻 4. Código y Comunicación Web
El Arduino se comunica mediante puerto serial (Firmata o WebSerial API) para traducir los valores físicos del potenciómetro y el botón en acciones dentro del juego web.

```cpp
// Ejemplo base de lectura de entradas
const int pinSlider = A0;
const int pinButton = 2;

void setup() {
  Serial.begin(9600);
  pinMode(pinButton, INPUT_PULLUP);
}

void loop() {
  int sliderValue = analogRead(pinSlider);
  int buttonState = digitalRead(pinButton);
  
  // Envío de datos al navegador
  Serial.print(sliderValue);
  Serial.print(",");
  Serial.println(buttonState);
  delay(50);
}
