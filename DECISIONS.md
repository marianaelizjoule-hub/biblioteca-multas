# Decisiones técnicas

## Decisión 1: validar los datos antes del cálculo

**Problema:** Si los días de retraso o la tarifa diaria son negativos,
el resultado de la multa sería incorrecto.

**Decisión:** Implementar validaciones antes de realizar el cálculo de
la multa.

**Justificación:** Garantiza que el programa solo procese datos válidos
y evita resultados inconsistentes o errores lógicos.

## Decisión 2: separar las validaciones en funciones independientes

**Problema:** Centralizar todas las validaciones dentro de una sola
función dificulta la lectura y el mantenimiento del código.

**Decisión:** Crear las funciones `validar_dias_retraso()` y
`validar_tarifa_diaria()` para verificar cada dato de entrada.

**Justificación:** Mejora la modularidad del código, facilita la
reutilización de las validaciones y hace más sencilla la localización
de errores.

## Decisión 3: utilizar excepciones para manejar errores

**Problema:** Retornar valores especiales o mostrar mensajes en pantalla
puede dificultar la detección de errores por parte de otras partes del
programa.

**Decisión:** Utilizar la excepción `ValueError` cuando los datos de
entrada sean inválidos.

**Justificación:** Las excepciones permiten informar errores de forma
clara, favorecen las buenas prácticas de programación y simplifican la
creación de pruebas automatizadas.

## Decisión 4: incorporar anotaciones de tipo y documentación

**Problema:** Sin documentación ni tipos explícitos, el código es más
difícil de comprender y mantener.

**Decisión:** Utilizar *type hints* y *docstrings* en todas las
funciones.

**Justificación:** Mejora la legibilidad del código, facilita el
mantenimiento y permite que herramientas como Pylint realicen
verificaciones más precisas.

## Decisión 5: automatizar las pruebas

**Problema:** Verificar manualmente el funcionamiento del programa
después de cada cambio consume tiempo y aumenta el riesgo de errores.

**Decisión:** Utilizar Pytest para comprobar los resultados esperados y
los casos de error.

**Justificación:** Permite ejecutar pruebas de forma rápida y
repetible, asegurando que las funcionalidades continúen funcionando
correctamente después de cada modificación.
