# Práctica 1 - TypeScript

Dos partes, mismo repo:

- **Parte 1** — tipos, arrays y callbacks (20 ejercicios).
- **Parte 2** — types/interfaces, clases, encapsulamiento y clases abstractas (ejercicios 7 a 13).

## Instalación

```bash
npm install
```

## Cómo trabajar

1. Completá cada función/método donde dice `// TODO`, en los archivos que se
   listan más abajo.
2. **No modifiques** los archivos `*.test.ts`, ni `src/db.ts`.
3. Corré los tests:

   ```bash
   npm test
   ```

   Al principio **casi todos los tests fallan** (las funciones y métodos
   tiran `Error("Implementar")`). A medida que vayas completando cada
   ejercicio, sus tests correspondientes van pasando en verde.

4. Modo watch (se re-ejecutan solos al guardar):

   ```bash
   npm run test:watch
   ```

5. Chequeo de tipos, sin ejecutar nada:

   ```bash
   npm run typecheck
   ```

## Parte 1 — tipos, arrays y callbacks

| Archivo | Contenido |
|---|---|
| `src/db.ts` | Datos de prueba (1000 alumnos) — **NO MODIFICAR** |
| `src/ejercicios.ts` | Los 20 ejercicios (1 a 20) |
| `src/ejercicios.test.ts` | Tests — **NO MODIFICAR** |

Reglas:
- Resolver usando métodos de arrays (`map`, `filter`, `find`, `some`, `every`, `reduce`) en lugar de `for`/`while`, siempre que el enunciado no pida explícitamente otra cosa.
- No mutar los arreglos originales.
- En los ejercicios con callback (15 a 18), la función debe recibir el callback como parámetro, tal como está tipado.

## Parte 2 — types, interfaces, clases y clases abstractas

| Ejercicio | Archivo | Tema |
|---|---|---|
| 7  | `src/ej07-tipos-interfaces.ts` | `type` vs `interface` |
| 8, 9, 10 | `src/clase-alumno.ts` | Clase `Alumno`: atributos, encapsulamiento, materias |
| 11 | `src/cuenta.ts` | Clase `Cuenta`: encapsulamiento y validaciones |
| 12 | `src/figuras.ts` | Clase abstracta `Figura` y polimorfismo |
| 13 | `src/empleados.ts` | Clase abstracta `Empleado` y polimorfismo |

`src/clase-alumno.ts` cubre tres ejercicios seguidos (8, 9 y 10) porque es
**la misma clase** evolucionando: primero los atributos básicos, después se
privatiza `edad` con su getter/setter, y por último se le agrega el manejo
de materias. Los tests están agrupados por ejercicio, así que se van
poniendo en verde por bloques a medida que avanzás.

`private` y `abstract` ya vienen puestos en el esqueleto de las clases: lo
que falta completar es el *cuerpo* de cada método.

`src/ej07-tipos-interfaces.ts` viene acompañado de
`src/RESPUESTAS-ejercicio7.md`: ahí van las respuestas de comparación entre
`type` e `interface` (esas preguntas no se corrigen con tests automáticos,
las lee el docente).

Reglas adicionales:
- No mutar arreglos/objetos internos de una clase desde afuera (por ejemplo,
  `getMaterias()` de `Alumno` debe devolver una copia).
- Las validaciones de `setEdad`, `depositar` y `retirar` deben lanzar un
  error (`throw new Error(...)`) ante un valor inválido, no devolver
  `false` ni ignorar el llamado silenciosamente.
- `Figura` y `Empleado` son clases abstractas: no se instancian directamente,
  solo sus subclases.
