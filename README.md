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
_____
```

## 8. Experimentos (Fase 3)

**Experimento A: ¿qué resultado dio `2 * ancho + alto` con 5 × 3? ¿Por qué?**
_____

**Experimento B: sin validación, ¿qué mostró el programa con ancho -4 y alto 3? ¿Tiene sentido?**
_____

**Experimento C (opcional): con `int`, ¿qué pasó con 2.5 y con 100000 × 100000?**
_____

## 9. Tabla de pruebas (Fase 4)

| Caso | Ancho | Alto | Esperado | Obtenido | ¿Pasó? |
|---|---|---|---|---|---|
| Normal | 5 | 3 | Área 15, perímetro 16 | _____ | _____ |
| Cuadrado | 4 | 4 | Área 16, perímetro 16 | _____ | _____ |
| Decimales | 2.5 | 4 | Área 10, perímetro 13 | _____ | _____ |
| Muy pequeño | 0.1 | 0.1 | Área 0.01, perímetro 0.4 | _____ | _____ |
| Ancho cero | 0 | 3 | vuelve a pedir el ancho | _____ | _____ |
| Alto negativo | 5 | -2 | vuelve a pedir el alto | _____ | _____ |
| Texto | `abc` | 3 | `leerDecimal` vuelve a pedir | _____ | _____ |
| Caso propio 1 | _____ | _____ | _____ | _____ | _____ |
| Caso propio 2 | _____ | _____ | _____ | _____ | _____ |

## 10. Bitácora de mejoras (Fase 4)

| # | ¿Qué falló o qué quise mejorar? | ¿Qué cambié? | ¿Funcionó? |
|---|---|---|---|
| 1 | _____ | _____ | _____ |
| 2 | _____ | _____ | _____ |

**Reto elegido (opcional):** _____

## 11. Dudas para el profesor (Fase 3)

| Duda | Lo que ya intenté |
|---|---|
| _____ | _____ |

## 12. Reflexión final

**¿Qué aprendí con esta práctica?**
_____

**Ahora que terminé, ¿qué cambiaría de mi proceso?**
_____

**¿Qué fue lo más difícil y cómo lo resolví?**
_____

**¿Qué pregunta me quedó sin responder?**
_____

**Diseñar la receta desde cero, ¿fue más fácil o más difícil de lo que esperaba? ¿Qué haría distinto la próxima vez?**
_____

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