# Práctica 1 - TypeScript: tipos, arrays y callbacks

## Instalación

```bash
npm install
```

## Cómo trabajar

1. Abrí [`src/ejercicios.ts`](src/ejercicios.ts) y completá cada función donde dice `// TODO`.
2. **No modifiques** [`src/db.ts`](src/db.ts) ni [`src/ejercicios.test.ts`](src/ejercicios.test.ts).
3. Corré los tests:

   ```bash
   npm test
   ```

   Al principio **todos los tests fallan** (cada función tira `Error("Implementar")`).
   A medida que vayas completando funciones, sus tests correspondientes van a ir
   pasando en verde. El objetivo es llegar a los 20 ejercicios en verde.

4. Para dejar los tests corriendo en modo watch (se re-ejecutan solos al guardar):

   ```bash
   npm run test:watch
   ```

5. Para chequear que el código tipa correctamente sin ejecutar nada:

   ```bash
   npm run typecheck
   ```

## Reglas

- Resolver usando métodos de arrays (`map`, `filter`, `find`, `some`, `every`, `reduce`) en lugar de `for`/`while`, siempre que el enunciado no pida explícitamente otra cosa.
- No mutar los arreglos originales.
- En los ejercicios con callback (15 a 18), la función debe recibir el callback como parámetro, tal como está tipado.

## Estructura

```
src/
  db.ts                 # Datos de prueba (1000 alumnos) — NO MODIFICAR
  ejercicios.ts         # Acá completás los 20 ejercicios
  ejercicios.test.ts    # Tests — NO MODIFICAR
```
