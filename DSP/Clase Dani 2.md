# Clase 2 - Dani
## Conclusiones Guía 1
- Si se carga algo al b (por ejemplo), se cargaría en principio en el b1, pero mata también la parte alta (es decir, es distinto de cargar directo en b1)
- Cargar algo en x directo no se puede (cargar x1 y x0 instead)
- Si quiero usar algo como un contador (no número fraccionario) uso '>'
- Si cargo algo en 'a' o en 'b' es una carga aritmética (completa con 0xff si es negativo) si cargo en 'a1' o 'b1' no completa
- Si es no signado hay que especificarlo
- ccr es la parte menos significativa de sr
- Los registros r son siempre no signados
- El registro Y es, por defecto, signado
- Scaling mode : shiftea luego de la operación
