# PENDIENTE · Publicar este repo en GitHub Pages

Estado: **preparado en local, sin subir**. Fecha de preparación: 2026-07-25.
Nada de esto está en línea todavía: las URL de abajo **aún no funcionan** hasta completar los pasos 1-4.

## Qué falta hacer (por orden)

1. **Crear el repositorio** `brandty-recursos` en la cuenta/organización de Brandty en GitHub (privado o público; Pages funciona en ambos con plan de pago, en cuenta gratuita el repo debe ser público).
2. **Subir esta carpeta completa** (incluidos `.nojekyll` y `CNAME`; sin ellos, GitHub ignora carpetas y se pierde el dominio propio).
3. **Activar Pages**: Settings → Pages → Source: *Deploy from a branch* → rama `main`, carpeta `/ (root)` → Save.
4. **DNS**: crear un registro **CNAME** `recursos` → `<usuario-github>.github.io` en el proveedor de dominio de Brandty. Después, en Settings → Pages, marcar **Enforce HTTPS** (tarda unos minutos en habilitarse).

## Comprobar antes de dar por bueno

- [ ] Los tres recursos cargan con **tipografía Jornada** (si se ve Arial, las fuentes no están sirviéndose).
- [ ] El **logo** aparece en `puntua-tu-consultora` y `mapa-decision`.
- [ ] El botón **"Guardar mi resultado en PDF"** abre el diálogo de impresión y el PDF sale limpio (sin el botón).
- [ ] Se ve bien en **móvil**.
- [ ] El código fuente incluye `<meta name="robots" content="noindex, follow">`.

## URL que quedarán activas

| Recurso | URL | Etiqueta | Va en |
|---|---|---|---|
| Auditoría Express | `https://recursos.brandty.es/auditoria-express/` | `lm-auditoria-express` | Email de acceso + página de entrega del MKT-02 |
| Puntúa tu consultora | `https://recursos.brandty.es/puntua-tu-consultora/` | `lm-puntua-consultora` | Email de acceso + página de entrega de su MKT-02 |
| Mapa de decisión | `https://recursos.brandty.es/mapa-decision/` | `lm-mapa-decision` | Entrega de captación fría |
| Índice | `https://recursos.brandty.es/` | — | Uso interno |

## ⚠ Regla importante para no romper la captación

Estas URL son de **ENTREGA**: solo se usan **después** de que la persona haya dejado sus datos y confirmado.

- En los **emails de nurturing** (MKT-04, MKT-05) el enlace debe ir a la **landing con formulario** (`go.brandty.es/...`), nunca al recurso directo. Si se enlaza el recurso, se regala sin captar el dato y se rompe el doble opt-in.
- Tampoco enlazar el recurso desde la landing indexable (regla del canon de landings §9).

## Otros pendientes relacionados

- Subir los **PDF rellenables** a Media Storage de GHL y anotar sus URL en `30_PROYECTOS\00_LEAD_MAGNETS\06_PDF_RELLENABLES_2026-07-24\README_ENTREGA_Y_URLS.md`.
- Crear la **landing `/puntua-tu-consultora`** en GHL (aún no existe) antes de activar MKT-04.
