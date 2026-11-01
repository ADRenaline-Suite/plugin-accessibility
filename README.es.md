<p align="right">Idioma:&emsp;<a href="README.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

# Accesibilidad (`plugin-accessibility`)

Audita un diseño o una pantalla construida contra WCAG 2.2, y escribe el requisito antes de que la pantalla se codifique. El objetivo es AA salvo que el producto haya fijado otro.

Las instrucciones están en inglés. El archivo que guarda el plugin sigue el idioma del pedido. Los archivos van en `adrenaline/accessibility/`.

## /a11y-design

El handoff o el mock, comprobado antes del código. Una nota de contraste que falta queda en hueco.

## /a11y-implementation

Una URL o una captura. Un escaneo automático es una pista, no conformidad.

## /a11y-requirements

Un criterio WCAG 2.2 y cómo se ve un aprobado.

## /a11y-notes

El nombre, el foco, el contraste y el tamaño del objetivo que quien construye debe conservar.

## Ayuda

## /a11y-help

El catálogo de este plugin. No escribe un archivo.

## Para quién es

Quien necesita una comprobación que quien construye puede cumplir. Las palabras quedan en `plugin-ux-writing`. El layout queda en `plugin-ui-ux-design`. El escenario de prueba queda en `plugin-qa-engineer`. Este plugin no copia sus skills.

## Qué incluye

Portable, para cualquier agente que siga [Agent Skills](https://agentskills.io/specification):

- `audit-accessibility` audita un diseño o una pantalla construida.
- `specify-accessibility` escribe el requisito y la nota que quien construye debe conservar.

Cursor y Claude Code: los commands de arriba. En Cursor, `/a11y-design`. En Claude Code, `/plugin-accessibility:a11y-design`.

Solo Cursor: las rules `output-folder`, `wcag-not-reinvented`. Claude Code no carga rules. Las mismas restricciones están en los skills.

## Instalar

En Cursor, instala el plugin desde este repositorio en Customize.

En Claude Code:

```text
claude plugin marketplace add ADRenaline-Suite/plugin-accessibility
claude plugin install plugin-accessibility@plugin-accessibility
```

Para probar una copia local, arranca Claude Code con `claude --plugin-dir <ruta de este repositorio>`.

## Ejemplo

Pide `/a11y-implementation` y da una URL. El archivo cita el criterio que falla. Un segundo idioma que no se comprobó queda en hueco.

## Configuración

Los archivos van en `adrenaline/accessibility/`. Una pantalla nombrada va en `<subject>/`. El objetivo es WCAG 2.2 AA salvo que el producto haya fijado otro.

## Licencia

MIT. Copyright (c) 2026 Ricardo Plascencia.

