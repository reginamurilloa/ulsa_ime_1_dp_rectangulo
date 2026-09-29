# Práctica 3: Área y perímetro de un rectángulo
## 1. Descripción del problema (Fase 1)
<!-- Explica con tus palabras qué hace tu programa y para qué serviría en la vida real. Máximo 4 líneas. -->
Este programa te ayudaria a sacar más facil el área y el perimetro de algun plano con las medidas que ya tenemos, ejemplo el terreno de una casa. 

_____

## 2. Entradas y salidas (Fase 1)
<!-- Define cada entrada y cada salida, con su tipo de dato, sus unidades y su objetivo. -->

**Entradas:**
1. dos datos: lado x lado 
2. dos datos: lado + lado + lado + lado

**Salidas:**
1. área
2. perímetro

**Fórmulas** (área y perímetro):
_____

## 3. Restricciones e invariante (Fase 1 y 2)

**Restricciones** (¿qué debe cumplirse?):
- no aceptar números negativos
- no aceptar el 0

**¿Qué hace mi programa con una medida de 0 o negativa? ¿Por qué?**
lo rechaza, por que no puede haber una medida de 0, en ese caso de seria un rectangulo

**¿Quién detecta cada error?** (¿qué revisa `leerDecimal` y qué reviso yo?)
Ayuda a identificar si no es un número como abc, algún dato no valido, y te vuelve a pedir la info

**Invariante** (al salir del ciclo que pide el ancho, ¿qué es seguro sobre `ancho`?):
asegurarse que sea un numero valido para calcular área y perímetro

## 4. Casos resueltos a mano (Fase 1)

| Caso | Ancho | Alto | Área calculada a mano | Perímetro calculado a mano |
|---|---|---|---|---|
| 1 | 4 | 3 | ÁREA: 12 | PERÍMETRO: 14 |
| 2 (cuadrado) | 5 | 5 | ÁREA: 25 | PERÍMETRO: 20 |
| 3 (con decimales) | 2.5 | 3 | ÁREA: 7.5 | PERÍMETRO: 11 |

## 5. Receta en pseudocódigo (Fase 2)
<!-- Tu receta va en el archivo RECETA.md. Aquí solo responde las preguntas. -->

**¿Probé mi receta a mano con un caso válido y uno inválido?** Si 
**¿Tuve que corregirla?** Si
**¿Cuántas versiones de mi receta escribí hasta la final?** 2, me falto agregar que no aceptara lo números negativos

## 6. Cómo compilar y ejecutar (Fase 3)

```bash
g++ -Wall -Wextra -std=c++17 main.cpp -o rectangulo
./rectangulo
```

## 7. Ejemplo de ejecución (Fase 3)
<!-- Pega aquí lo que muestra tu programa en pantalla con un caso normal. -->

```
Area y perimetro de un rectangulo
Introduce el ancho del rectangulo: 8
Introduce el alto del rectangulo: 5
El area del rectangulo es: 40 unidades cuadradas.
El perimetro del rectangulo es: 26 unidades.
```

## 8. Experimentos (Fase 3)

**Experimento A: ¿qué resultado dio `2 * ancho + alto` con 5 × 3? ¿Por qué?**
Area y perimetro de un rectangulo
Introduce el ancho del rectangulo: 5
Introduce el alto del rectangulo: 3
El area del rectangulo es: 15 unidades cuadradas.
El perimetro del rectangulo es: 13 unidades.

Porque el 2 * ancho + alto, solo esta multiplicando al ancho y el alto solo lo suma 1 vez. De esta manera da un resultado incorrecto

**Experimento B: sin validación, ¿qué mostró el programa con ancho -4 y alto 3? ¿Tiene sentido?**
Area y perimetro de un rectangulo
Introduce el ancho del rectangulo: -4
El ancho debe ser mayor que 0. Intenta de nuevo.Introduce el ancho del rectangulo:

Marca error ya que mi codigo no acepta números negativos



## 9. Tabla de pruebas (Fase 4)

| Caso | Ancho | Alto | Esperado | Obtenido | ¿Pasó? |
|---|---|---|---|---|---|
| Normal | 5 | 3 | Área 15, perímetro 16 | área 15, perímetro 16 | si |
| Cuadrado | 4 | 4 | Área 16, perímetro 16 | área 16, perímetro 16 | si |
| Decimales | 2.5 | 4 | Área 10, perímetro 13 | área 10, perímetro 13 | si |
| Muy pequeño | 0.1 | 0.1 | Área 0.01, perímetro 0.4 | área 0.01, perímetro 0.4 | si |
| Ancho cero | 0 | 3 | vuelve a pedir el ancho | El ancho debe ser mayor que 0. Intenta de nuevo.| si, marco error en el codigo y te pide que ingreses otro número|
| Alto negativo | 5 | -2 | vuelve a pedir el alto | El alto debe ser mayor que 0. Intenta de nuevo. | si, marco error en el codigo y te pide que ingreses otro número |
| Texto | `abc` | 3 | `leerDecimal` vuelve a pedir | Entrada no valida. Escribe un numero (ej. 5 o 2.5) | si, aparece que pongas un número que sea valido |
| Caso propio 1 | 22 | 8 | Área 176, Perímetro 60 | área 176, perímetro 60 | si |
| Caso propio 2 | 2.3 | 0 | vuelve a pedir el alto | El alto debe ser mayor que 0. Intenta de nuevo. | si |

## 10. Bitácora de mejoras (Fase 4)

| # | ¿Qué falló o qué quise mejorar? | ¿Qué cambié? | ¿Funcionó? |
|---|---|---|---|
| 1 | hacer el codigo facil para utilizar | explicaciones mas claras | si |



## 11. Dudas para el profesor (Fase 3)

| Duda | Lo que ya intenté |
|---|---|
| ninguna |  |

## 12. Reflexión final

**¿Qué aprendí con esta práctica?**
A crear el codigo de manera más facil y guiarme de mis trabajos anteriores

**Ahora que terminé, ¿qué cambiaría de mi proceso?**
intentar no guiarme tanto de is trabajos anteriores y confiar más en mi

**¿Qué fue lo más difícil y cómo lo resolví?**
hacer el main.cpp 
Revisando mis trabajos y haciendo pruebas de como funcionaba el codigo 

**¿Qué pregunta me quedó sin responder?**
ninguna

**Diseñar la receta desde cero, ¿fue más fácil o más difícil de lo que esperaba? ¿Qué haría distinto la próxima vez?**
Fue facil relativamente, podria más atención para hacer más rapido el codigo

## 13. Lista de verificación antes de entregar (Fase 5)

- [ ] Llené todas las secciones (no quedan `_____`)
- [ ] Escribí mi receta completa en `RECETA.md` antes de programar
- [ ] Mi programa compila sin advertencias
- [ ] Probé todos los casos de la tabla
- [ ] Hice los Experimentos A y B y dejé el código correcto al terminar
- [ ] No modifiqué `utilerias.h`
- [ ] Hice al menos 3 commits con mensajes claros
- [ ] Hice `git push` y verifiqué mi fork en GitHub
- [ ] Entregué el enlace de mi fork en Classroom