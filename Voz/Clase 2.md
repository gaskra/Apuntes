# Fiambres
## El aparato fonador
- Existen órganos de respiración, fonación y articulación dentro del aparato fonador. Recordar que estos órganos tienen múltiples funciones a parte de las mencionadas.
- Fuente de corriente (flujo continuo de aire gracias a los órganos de respiración), rectificador y filtro sería el equivalente en términos elecrónicos
- El camino (tráquea) a los pulmones es rígido. De no serlo, sería fácil que se tapara la vía respiratoria lo cual sería un problema vital. No ocurre lo mismo en el camino que va al estómago
- Los pulmones funcionan por una diferencia de presión
- En una buena simulación de voz, se notaría la respiración (debe ser modelado correctamente)
- La laringe (órgano de fonación) produce el fenómeno de Bernoulli que concluye en un proceso de rectificación (transforma una señal continua de aire en una alterna)
- Un sonido __sonante__ es aquel en el que las cuerdas vocales se activan
- Los órganos de articulación filtran la señal alternada y permite producir diferentes vocales
- El __diafragma__ es el encargado de contraer y expandir el pulmón
- Lo que contiene la caja toráxica es lo más importante para la vida
- El hipo es una contracción involuntaria del diafragma
- La __epíglotis__ es la que se encarga de determinar si lo que ingresa pasa al aparato digestivo o no
- La lengua ayuda a modular las señales aeróbicas, define un filtro pasa-banda
- El __aparato fonador__ tiene muchos músculos. La epíglotis protege a este aparato de sólidos y/o líquidos
- Los músculos solamente pueden contraerse
- Hay un punto en el aparato fonador que de mueve con varios músculos y determinan el tono (frecuencia)
-  Las cuerdas vocales con pieles con mucosidad para que se mantengan húmedas
- Hay cuerdas vocales verdaderas y falsas (las solo producen una resonancia pero no vibran)
- La __glotis__ es la apertura entre las cuerdas vocales (es simplemente un agujero que se encuentra en la laringe)
- Las cuerdas vocales se tensan cuando uno habla
- 12 a 17 y 17 a 25 es el espesor de las cuerdas vocales en mm de mujeres y hombres respectivamente. Está directamente relacionado con la frecuencia de la voz
- Las cuerdas vocales se pueden modelar como un conjunto de tubos de distinto diámetro
- El aparato fonador se puede modelar como un ARMA
- La lengua tiene muchas fibras, por lo cual se puede mover de muchas formas y permite generar múltiples sonidos diferentes
- Los dientes al ser duros tienen una impedancia distinta al aire, provocando mucho rebote. Explica por qué se pueden producir sonidos que no salen de la faringe ('shhh')
- Sonidos como 'f' y 's' dependen de los dientes
- La interacción labios y dientes permite modificar la frecuencia del pasa-banda de sonidos como el 'shh'
- Los labios regulan la interacción entre los sonidos que provienen del interior al exterior

## Fonética articulatoria
- Cuando se susurra no se activan las cuerdas sonóras
- La primera clasificación es
  - _sonoros_ : los que activan las cuerdas
  - _sordos_ : no activan las cuerdas
- El __punto de articulación__ es el lugar de máximo estrechamiento.
  Ej. i : zona 8
- __Vocales__ : no hay obstrucción en las cavidades (apertura de la boca, labios y puntos de articulación)
- Una __formante__ es una frecuencia con mucha energía
- Hay relación entre la formante y las vocales. Se podrían distinguir en principio mirando la frecuencia
- Los sonidos "clics" tienen poca energía y baja duración. Los sonidos sonoros son más fáciles de reconocer. Es importante el contexto para una muy buena detección.
- __Consonantes__:
  - Obstruyentes : Tienen una obstrucción en el trayecto de aire
    - Oclusivas : oclusión y liberación de energía (P,T,C). Corta duración. Difíciles de reconocer. Baja energía  
    - Fricativas : Son turbulentas (S,F,J)
    - Africadas : Empiezan oclusivas y siguen fricativas (CH,X)
  - Sonantes : Consonantes sonóras (obstrucción + activación de cuerdas)
    - Nasales: El sonido sale por la nariz casi en totalidad (M,Ñ)
    - Líquidas: Parte de la cavidad está ocluida (L,R)
    - Aproximantes : El punto de articulación está ocluído pero no totalmente (B,D,G)
  - No-pulmonar :
    - Eyectivas
    - Implosivas
    - Chasquidos (clics)
- Acento
  - Lexical : es el que va escrito
  - Prosódico : es para enfatizar en el habla


## Modelado del mecanismo de producción de voz
- No es posible mantener un sonido en el aire constante (hay al menos mínimas variaciones de tono y volumen)
- Las fuentes periódicas estacionarias suenan de forma metálica
- Mecanismo de __Bernoulli__ se produce gracias a una mucosa que puede cerrar o dejar pasar el aire y puede _choppearlo_ en pulsos separados
- 80 a 150, 150 a 300 son los rangos en Hz de hombres y mujeres respectivamente
- El espectro de los pulsos glotales es pasabajo de primer orden al principio. Sin embargo, no es un filtro de primer orden porque la caida no es pareja después. Además tiene alinealidades
- Los pulsos glotales son localmente estacionarios, pero suprasegmentalmente no
- La voz no puede cambiar de tono bruscamente
- Se tarda mas o menos 10-20 ms para cambiar de tono rápidamente
- Se va a obviar la parte nasal para el modelado del tubo en este curso
- La secuencia de tubos se representa por IRR
- Los filtros Lattice representan la reflexión y transmisión de los tubos de diferente diámetro. Consideramos que cada tubo tiene espesor fijo
- Los diámetros de nuestros modelos no coincidirán con los reales ya que ignoramos la naríz
- Utilizando LMS se puede utilizar para predecir los parámetros de forma muy buena
- El modelo viste en clase sirve también para modelar sonidos 'shh' a pesar de en la realidad la configuración necesaria para producirlos es distinta