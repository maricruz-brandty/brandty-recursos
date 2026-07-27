# brandty-recursos

Recursos interactivos (lead magnets) de Brandty, servidos como páginas estáticas.

## Qué contiene

| Ruta | Recurso | Función | Uso |
|---|---|---|---|
| `/auditoria-express/` | Auditoría Express · Selección × Valores® | Semáforo de 40 puntos: se marca cada ítem, suma sola y da color | Objeción "lo hacemos en interno" (MKT-05) |
| `/puntua-tu-consultora/` | Puntúa el último proceso de tu consultora | 12 señales + interpretación | Objeción "ya trabajo con otra consultora" (MKT-04) |
| `/mapa-decision/` | Antes de contratar: mapa de decisión | Marco de 30 min para una posición crítica | Captación fría / orgánica (RRSS, ads) |
| `/` | Índice | Lista simple de recursos | — |

Cada recurso lleva un botón flotante **"Guardar mi resultado en PDF"** que abre el diálogo de impresión del navegador con los estilos de impresión aplicados: la persona se lleva su diagnóstico **con sus respuestas ya rellenadas**.

## Publicar en GitHub Pages

1. Crear repo `brandty-recursos` en la organización/cuenta de Brandty y subir esta carpeta.
2. Settings → Pages → Source: `Deploy from a branch`, rama `main`, carpeta `/ (root)`.
3. Dominio propio: el archivo `CNAME` ya apunta a `recursos.brandty.es`. En el DNS de Brandty, crear un registro **CNAME** `recursos` → `<usuario>.github.io`.
4. Esperar propagación y activar **Enforce HTTPS** en Settings → Pages.

El archivo `.nojekyll` evita que GitHub Pages procese los ficheros con Jekyll (necesario para que no ignore carpetas ni assets).

## URLs finales (para los workflows de GHL)

| Recurso | URL | Etiqueta |
|---|---|---|
| Auditoría Express | `https://recursos.brandty.es/auditoria-express/` | `lm-auditoria-express` |
| Puntúa tu consultora | `https://recursos.brandty.es/puntua-tu-consultora/` | `lm-puntua-consultora` |
| Mapa de decisión | `https://recursos.brandty.es/mapa-decision/` | `lm-mapa-decision` |

Estas URL van en el **email de entrega** del workflow correspondiente, junto al PDF rellenable:

> **Hazla online** → enlace de arriba (interactiva, suma sola)
> **Descárgala en PDF** → enlace del PDF en Media Storage de GHL

## Decisiones técnicas

- **`noindex, follow`** en todos los recursos: la landing es la que debe posicionar en Google, no el recurso. Regla del canon de landings (§9).
- **Fuentes Jornada Sans** servidas desde `/assets/fonts/` y declaradas en cada página, para que la tipografía corporativa cargue también fuera del ordenador de Brandty.
- **Sin control de acceso**: la URL es pública para quien la tenga, igual que un PDF en Media Storage. El control real lo da el doble opt-in del formulario, no la URL.
- Los HTML originales editables siguen en `30_PROYECTOS\00_LEAD_MAGNETS\01_…` y `02_…`. **Este repo es la copia publicable**: si se edita un recurso, actualizar aquí y hacer commit.

## Mantenimiento

Cualquier cambio de copy o de puntuación se hace en el HTML de este repo y se publica con un commit. No hace falta tocar GHL: las URL no cambian.
