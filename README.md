# tienda.funkypunkymc

Página de la tienda de **FUNKY PUNKY MC** (`tienda.funkypunky.lat`, en Vercel). Un solo `index.html`, sin compilar.

## Cambiar precios o duración
En `index.html`, al inicio del `<script>`:

```js
const PRECIOS_MXN = { vip: null, vipplus: null, gold: null };   // ej. { vip: 50, vipplus: 100, gold: 180 }
const DURACION = "Por 30 días";                                      // ej. "Permanente" o "Por 30 días"
```
Mientras un precio sea `null`, la tarjeta dice "Precio próximamente".
**Regla:** lo que dice la página debe ser igual a lo que da cada grupo de LuckPerms (vip, vip+, funky).

## Agregar a alguien al Top apoyadores
Editar `donadores.json` (lista; se ordena sola por `total`, que **no** se muestra en la página):

```json
[
  { "nombre": "SAULPLAY112", "rango": "gold", "total": 180 },
  { "nombre": ".JugadorBedrock", "rango": "vip", "total": 50 }
]
```
- `rango`: `vip`, `vipplus` o `gold` (el más alto que haya comprado).
- `total`: suma en MXN de todo lo que ha apoyado (si compra otra vez, se suma aquí).
- Solo agregar a quien **aceptó** salir en el top (pregúntale en su ticket).
- Validar el JSON antes de subirlo (una coma de más deja el top vacío).

## Archivos
- `logo.webp` (512 px), `favicon.png` (64 px), `og.jpg` (vista previa al compartir el enlace).
