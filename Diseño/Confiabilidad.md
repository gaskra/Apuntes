# Confiabilidad
## Introducción
- La confiabilidad me indica la probabilidad de que el elemento va a cumplir con la función requerida bajo determinadas condiciones en un intervalo de tiempo dado
- Un elemento es una unidad funcional que puede ser considerada una entidad a parte. Hay distintos niveles en los que hay que ir viendo cómo se cumplen las funciones
- Las funciones es lo que tiene que hacer un elemento
- Las condiciones es el contexto en el que puede ser utilizado un elemento para que cumpla con su función como fue especificado
- El tiempo es el parámetro fundamental de la confiabilidad. La confiabilidad en tiempo 0 es 1. Cuando t tiende a infinito, es 0. Se trata de que los equipos sean obsoletos antes de que fallen
- Una falla es que un elemento deje de cumplir la función para la cual fue hecho
- El modo de falla es el síntoma por el cual es detectada
- Causa : es el por qué de la falla (intrínseca, fallo del material, extrínseca, lo usaron mal y falló)
- Efecto : lo que produce la falla en consecuencia. Puede ser
  - No relevante
  - Parcial
  - Completa
  - Crítica
  - Primaria / Secundaria : Las secundarias derivan de otras fallas
- Fallas por desgaste. Ej. los electrolíticos
- Velocidad de aparición de fallas (repentinas o progresivas, en electrónica por ej. la temperatura)
- Según el grado : parciales y no completas
- Fallas que "parecen que se arreglaron" : fallas intermitentes. Ej. problema de contactos

## Clasificación
- Fallas por degradación o paramétricas : progresivas o parciales
- Fallas catastróficas : repentinas, completas y definitivas

## Fallas catastróficas
- Ver deducción de fallas
- Tasa de Fallas : proporción de elementos que pueden fallar entre t y delta(t)
- Se define el tiempo a la falla. Es mucho más útil porque muchos productos ya cuando fallan una vez dejan de ser útiles (vs tiempo medio entre fallas)
- Estudiar la demo de MTTF
- Si lambda es constante, MTTF = 1/lambda
- Mortalidad infantil : asociado con las fallas iniciales
- Curva de la bañera
- En el medio de la bañera es lambda constante (tiempo de vida útil)
- En general, en eletrónica los elementos se hacen obsoletos antes de entrar en Wearout
- Cuando una empresa recién arranca, es común que la tasa de mortalidad infantil sea elevada
- Fallas tempranas, accidentales y envejecimiento
- La distribución que caracteriza la sección de lambda constante es Poisson

## Estimación de Confiabilidad
- Ver receta del PPT
- En diagrama de confiabilidad es sobre eventos
- No es lo mismo el diagrama funcional qu eel diagrama de eventos
- Factor de estrés. Puede ser que de mayor a 1 por un tiempo determinado
- Condición de operación
- Estudiar apunte de tasa de falla
- El lambda en la norma está en 10-6 horas
- En la actualidad está en FIT (10-9)
- Método de conteo de partes : considerar en una primera aproximación que los lambda de los mismos elementos son iguales
- Método de las cargas : considera las cargas de cada elemento en particular
- En los paralelos es la suma menos la intersección. Ver fórmula con binomial
- Todo aquel elemento de conmutación tiene doble modalidad de falla (que salte cuando no debería, que no salte cuando debería saltar)
- El conmutador debe tener <10% de la tasa de fallas de los elementos a salvar
