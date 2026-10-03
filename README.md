# Calculadora WEB — Tarea 2

**Curso:** Programación WEB (2026-C-003)
**Profesor:** Raydelto Hernández — ITLA
**Puntuación:** 8 puntos

## Descripción

Calculadora web con interfaz de sumadora de escritorio y una "cinta de papel" lateral
que registra el historial de operaciones. Permite realizar las cuatro operaciones
básicas (suma, resta, multiplicación, división) y conserva el historial entre
sesiones usando `localStorage`, hasta que el usuario decide borrarlo.

## Archivo

- `calculadora.html` — Archivo único y autocontenido (HTML + CSS + JavaScript).
  No requiere instalación, dependencias ni servidor: se abre directamente en
  cualquier navegador moderno haciendo doble clic sobre él.

## Tecnologías utilizadas

| Tecnología | Uso |
|---|---|
| HTML5 | Estructura del teclado, pantalla y cinta de historial |
| CSS3 | Estilo visual (gradientes, grid, sombras, diseño responsivo) |
| JavaScript (ES5) | Lógica de la calculadora y manejo del historial |
| `localStorage` | Persistencia del historial de cálculos en el navegador |

> El JavaScript se escribió deliberadamente en **ES5** (`var`, funciones
> declaradas, sin arrow functions ni `let`/`const`) para ajustarse al tema de
> la semana correspondiente en el cronograma del curso.

## Funcionalidades

- [x] Operaciones básicas: suma (+), resta (−), multiplicación (×) y división (÷)
- [x] Pantalla principal y pantalla secundaria (operación en curso)
- [x] Historial de cálculos guardado en `localStorage`
- [x] Botón **"Borrar cinta"** para eliminar el historial guardado
- [x] Manejo de error en división entre cero
- [x] Botones de limpiar (`AC`) y borrar último dígito (`⌫`)
- [x] Soporte de teclado (números, operadores, `Enter`, `Backspace`, `Esc`)
- [x] Diseño responsivo (se adapta a pantallas pequeñas)

## Cómo usarlo

1. Abrir `calculadora.html` en el navegador.
2. Introducir el primer número con los botones o el teclado.
3. Elegir una operación (÷, ×, −, +).
4. Introducir el segundo número y presionar `=` (o `Enter`).
5. El resultado aparece en pantalla y la operación se agrega a la cinta de
   historial, a la derecha (o debajo, en pantallas angostas).
6. Para limpiar el historial guardado, usar el botón **"Borrar cinta"**.

## Notas de implementación

- El historial se guarda como un arreglo JSON bajo la clave
  `itla_calc_historial` en `localStorage`, por lo que persiste al recargar
  la página o cerrar el navegador (pero es local a cada navegador/dispositivo).
- Toda la lógica de cálculo evita el uso de `eval()`, procesando la operación
  mediante una función `calculate(a, b, operador)`.
- El archivo es completamente autónomo: no depende de librerías externas de
  JavaScript, solo de dos tipografías de Google Fonts para el estilo visual.
