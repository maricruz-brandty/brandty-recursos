# ESTADO · Publicación en GitHub Pages

Estado: **repositorio, Pages y DNS operativos; certificado HTTPS pendiente**. Actualizado: 2026-07-27.

- Repo público: `https://github.com/maricruz-brandty/brandty-recursos`
- Rama y origen de Pages: `main` · `/ (root)`
- Build verificado: último commit de `main`, estado `built` el 2026-07-27
- Dominio configurado en GitHub Pages: `recursos.brandty.es`
- DNS verificado: `recursos.brandty.es` → `maricruz-brandty.github.io`
- Bloqueo actual: GitHub todavía está emitiendo el certificado; las cuatro rutas responden por HTTP, pero falta activar HTTPS.

## Qué falta hacer (por orden)

1. [x] Crear el repositorio público `maricruz-brandty/brandty-recursos`.
2. [x] Subir la carpeta completa, incluidos `.nojekyll` y `CNAME`.
3. [x] Activar Pages desde `main` y `/ (root)`.
4. [x] Crear **CNAME** `recursos` → `maricruz-brandty.github.io`.
5. [ ] Cuando GitHub termine de emitir el certificado, activar **Enforce HTTPS**.

## Comprobar antes de dar por bueno

- [ ] Los tres recursos cargan con **tipografía Jornada** (si se ve Arial, las fuentes no están sirviéndose).
- [ ] El **logo** aparece en `puntua-tu-consultora` y `mapa-decision`.
- [ ] El botón **"Guardar mi resultado en PDF"** abre el diálogo de impresión y el PDF sale limpio (sin el botón).
- [ ] Se ve bien en **móvil**.
- [x] El código fuente incluye `<meta name="robots" content="noindex, follow">`.

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

## Otros elementos relacionados ya resueltos

- [x] Los tres **PDF rellenables** están en Media Storage de GHL y sus URL constan en `30_PROYECTOS\00_LEAD_MAGNETS\06_PDF PARA ENTREGAR (rellenables) 2026-07-24\LEEME - entrega y URLs.md`.
- [x] La landing **Puntúa tu consultora** está publicada en `https://go.brandty.es/puntua-tu-consultora-518560`. MKT-04 sigue en borrador y no debe activarse hasta completar sus pruebas.

---

## PUBLICADO Y AUDITADO 27-jul · mapa de flujos

Estado: **publicado en GitHub Pages el 2026-07-27** en
`https://recursos.brandty.es/mapa-flujos/`. El contenido ya está desplegado, pero la comprobación
final por HTTPS sigue pendiente hasta que GitHub emita el certificado del dominio.

Última auditoría y sincronización del contenido: **2026-07-27**. Se contrastó el mapa con GHL en
vivo y con las URL públicas. El mapa distingue ahora entre **verificado en vivo**,
**existe/parcial/sin prueba integral** y **diseñado o pendiente**. No se considera operativo un
workflow solo por figurar como Publicado.

Objetivo: que Mari y el implementador miren siempre la misma versión, en vez de pasarse el archivo
por WhatsApp.

1. [x] Copiar `30_PROYECTOS\MAPA_FLUJOS_GHL\index.html` a `/mapa-flujos/index.html` dentro de este repo.
2. [x] Comprobar que lleva `<meta name="robots" content="noindex, follow">`.
3. [x] Mantenerlo sin enlaces desde el índice del sitio ni desde otras páginas.
4. [x] Verificar localmente que se ve el plan con las tareas cerradas, aparece el registro de
   cambios y las cajas del diagrama abren su panel lateral.
5. [ ] Verificar la URL por HTTPS y repetir la comprobación de interacción cuando GitHub emita el certificado:
   `https://recursos.brandty.es/mapa-flujos/`.

**Recordatorio de mantenimiento:** cada vez que se actualice el mapa original, volver a copiar
`30_PROYECTOS\MAPA_FLUJOS_GHL\index.html` sobre `mapa-flujos/index.html`, comprobar que conserva
el `noindex`, subir el cambio y verificar de nuevo la URL pública.

**Por qué noindex y sin enlazar:** el mapa contiene detalle operativo interno (identificadores de
formulario, URL del calendario, lógica de los workflows, decisiones de negocio). No es información
secreta, pero tampoco conviene que la encuentre cualquiera en Google. Si se quiere control real de
acceso, la alternativa es un repositorio privado, que exige plan de pago para publicar páginas.
