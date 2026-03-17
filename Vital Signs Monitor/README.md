# Diseño de PCB: Data Logger de Signos Vitales 
Este proyecto consiste en el diseño y ruteo de una PCB para un Data Logger de Signos Vitales

## Vistas del Proyecto

<p align="center">
  <img src="Images/3D_1.png" width="45%" title="Vista 3D">
  <img src="Images/3D_2.png" width="45%" title="Vista 3D">
</p>

## Criterios de Diseño Aplicados

Durante el ruteo de la placa, los criterios de diseño que se tomaron para garantizar la estabilidad del circuito fueron:

* **Desacople de Alimentación Vcc:** Ubicación de capacitores cerámicos de 100nF en los pines de +Vcc y -Vcc para mitigar los efectos del ruido de alta frecuencia en la entrada de la alimentación del Op. Amp.
* **Plano GND en la Top Layer:** Implementación de un plano de masa continuo (*GND Pour*) en la capa Top para blindar el circuito y reducir significativamente las corrientes de retorno.

## Ruteo de Capas (Top & Bottom)

<p align="center">
  <img src="Images/2D_TOP.png" width="45%" title="Capa Top - Plano de Masa">
  <img src="Images/2D_BOTTOM.png" width="45%" title="Capa Bottom - Pistas de Señal">
</p>


