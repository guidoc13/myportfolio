# Diseño de PCB: Filtro Analógico Activo (Low Pass & Notch) con TL072

Este proyecto consiste en el diseño y ruteo de una placa de circuito impreso (PCB) para un filtro activo de audio utilizando el amplificador operacional dual TL072. El objetivo principal fue aplicar buenas prácticas de diseño orientado a la manufactura (DFM), integridad de señal y diseño para ensamblaje (DFA).

## Vistas del Proyecto

<p align="center">
  <img src="Images/3D_1.png" width="45%" title="Vista 3D Top">
  <img src="Images/3D_2.png" width="45%" title="Vista 3D Bottom">
</p>

## Criterios de Diseño Aplicados

Durante el ruteo de la placa, se tomaron decisiones técnicas específicas para garantizar la estabilidad del circuito y facilitar su posterior armado físico:

* **Integridad de Señal Analógica:** Implementación de *Star Routing* (nodo en estrella) en el lazo de realimentación del Op-Amp. Esto evita que las corrientes de retorno interfieran entre sí, minimizando el ruido y la impedancia compartida.
* **Estrategia de Desacople de Alimentación:** Ubicación crítica de capacitores cerámicos de 100nF en los pines de +Vcc y -Vcc. Se priorizó acortar el lazo de corriente de alta frecuencia cruzando de capa mediante el uso de una vía (via) estratégica justo al lado del pin de alimentación.
* **Inmunidad al Ruido (EMI):** Implementación de un plano de masa continuo (*GND Pour*) en la capa superior (Top) para blindar el circuito analógico y reducir significativamente los lazos de retorno.
* **Diseño para Ensamblaje (DFA):** Se anticipó la limitación física de soldar componentes con zócalos DIP en placas simple/doble faz de fabricación casera. Se optimizó el ruteo en la capa Bottom tomando la masa directamente desde el pad de un capacitor adyacente, evitando obstrucciones físicas para el soldador.
* **Estándares DFM:** Ruteo estandarizado con ángulos a 45° y pistas de 0.8 mm para las señales analógicas, garantizando una bajísima impedancia y robustez mecánica frente a la fabricación y soldado manual.

## Ruteo de Capas (Top & Bottom)

<p align="center">
  <img src="Images/2D_GND_top.png" width="45%" title="Capa Top - Plano de Masa">
  <img src="Images/2D_bottom.png" width="45%" title="Capa Bottom - Pistas de Señal">
</p>
