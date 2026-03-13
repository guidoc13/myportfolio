# Diseño de PCB: Filtro Analógico Activo (Low Pass & Notch) con TL072
Este proyecto consiste en el diseño y ruteo de una PCB para un Filtro Analógico Activo del tipo Pasa Bajos y Notch utilizando el Amplificador Operacional TL072. El objetivo principal fue realizar el análisis de respuesta en frecuencia empleando un Analizador de Redes.    

## Vistas del Proyecto

<p align="center">
  <img src="Images/3D_1.png" width="45%" title="Vista 3D Top">
  <img src="Images/3D_2.png" width="45%" title="Vista 3D Bottom">
</p>

## Criterios de Diseño Aplicados

Durante el ruteo de la placa, los criterios de diseño que se tomaron para garantizar la estabilidad del circuito fueron:

* **Desacople de Alimentación Vcc:** Ubicación de capacitores cerámicos de 100nF en los pines de +Vcc y -Vcc para mitigar los efectos del ruido de alta frecuencia en la entrada de la alimentación del Op. Amp.
* **Plano GND en la Top Layer:** Implementación de un plano de masa continuo (*GND Pour*) en la capa Top para blindar el circuito y reducir significativamente las corrientes de retorno.

## Ruteo de Capas (Top & Bottom)

<p align="center">
  <img src="Images/2D_GND_top.png" width="45%" title="Capa Top - Plano de Masa">
  <img src="Images/2D_bottom.png" width="45%" title="Capa Bottom - Pistas de Señal">
</p>

## Respuesta en frecuencia de cada filtro

<p align="center">
  <img src="Images/FrecResponse_LP.png" width="45%" title="Respuesta en Frecuencia haciendo uso del Analizador de Redes (Low-Pass)">
  <img src="Images/FrecResponse_NCH.png" width="45%" title="Respuesta en Frecuencia haciendo uso del Analizador de Redes (Notch)">
</p>

