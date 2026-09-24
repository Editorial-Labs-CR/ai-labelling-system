# Changelog

Versions are the `APP.version` value shown in the footer and in «About».
Las versiones son el valor `APP.version` que aparece en el pie y en «Acerca de».

## 20 — 2026-09-24

Cambios sobre la 19, que ya estaba publicada. Changes on top of the published 19.

- El **idioma de la etiqueta y la prosa se escoge primero**, en «Antes de empezar»; la URL
  del QR pasa a opciones de producción.
- Los dos ejes de idioma se distinguen en pantalla: «Idioma de la herramienta» arriba,
  «Idioma de la etiqueta y la prosa» abajo. El primero no tenía rótulo visible.
- **Se explica cuál es el umbral de declarabilidad**, que antes se nombraba sin definir:
  etiqueta «UMBRAL · OPCIONAL» junto a la actividad 1, nota junto a la lista de tareas,
  sección «Qué se declara y qué no» en el manual, y dentro de la propia prosa de N, que
  se publica con el artículo.
- La actividad 1 muestra en su fila los ejemplos y el «no incluye» de la lámina de STM,
  que es lo que la separa de la actividad 2.
- El **QR apunta a la app publicada**.
- Se declara la **codificación asistida por IA** con la fórmula de las demás herramientas
  del autor.
- Metadatos de vista previa (Open Graph, Twitter Card) e imagen de 1200×630 para
  compartir el enlace. El `<title>` del archivo llevaba el nombre anterior del sistema.
- Redacción: comillas dobles, sin guiones largos haciendo de paréntesis, sin siglas sin
  explicar y sin números de sección del artículo en el texto visible.

Correcciones / fixes:

- Dos casos de la batería usaban el código `GE`, retirado en favor de `TG`: se ignoraban
  en silencio y no probaban lo que decían probar.
- La batería se detenía **sin conexión** al comprobar los avisos del QR. Ahora el bloque
  que depende de la librería se **omite**, se informa en el registro y el resto termina.

Batería: **1299 aserciones con conexión · 1290 sin conexión**, con un bloque omitido.
La cifra de la entrada 19 (1282) era la correcta en su momento y se deja como está.

## 19 — 2026-09-23 · first public release / primera publicación

Versions 1–18 were internal iterations and are not published.
Las versiones 1–18 fueron iteraciones internas y no se publican.

State at first release / Estado en la primera publicación:

- Label and prose generated from a single declarative act, verified to agree on 600
  reconstructed cases.
- Two language axes: interface language and label language, independent of each other.
  The **code is invariant in English** in both; only the descriptions follow the label
  language. Spanish and English offered; Portuguese translated and tested but held back
  pending review by a native speaker (`LANGS` in the source).
- Constant label height across languages, so labels align on a page.
- Content-driven width from measured text; no magic numbers.
- Optional extent axis, optional tools and models, reserved space for a future third axis.
- QR guard against the silent truncation of the QR library past its capacity.
- Test suite of 1282 assertions, run with `window.__app.runSelfTest()`.

Known limitations / Limitaciones conocidas:

- The QR points to the published app itself. A journal that adopts the system will
  normally replace it with its own editorial policy page. A printed QR cannot be revoked,
  so check the address before going to print.
- The QR needs a connection: the library is loaded from a CDN.
- One description departs on purpose from the preprint that documents the system (`RF`);
  the divergence is declared in the test suite.
