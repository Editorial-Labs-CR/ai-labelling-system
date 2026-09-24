# Changelog

Versions are the `APP.version` value shown in the footer and in «About».
Las versiones son el valor `APP.version` que aparece en el pie y en «Acerca de».

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

- **The QR still points to a placeholder address.** It will be repointed at this app once
  it is live. A printed QR cannot be revoked, so do not print a definitive label yet.
- The QR needs a connection: the library is loaded from a CDN.
- One description departs on purpose from the preprint that documents the system (`RF`);
  the divergence is declared in the test suite.
