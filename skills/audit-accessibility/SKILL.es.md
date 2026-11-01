---
name: audit-accessibility
description: Audita un diseño o una pantalla construida contra WCAG 2.2 AA.
---

<p align="right">Idioma:&emsp;<a href="SKILL.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Accessibility](../../README.md)

# Audita un diseño o una pantalla construida contra WCAG 2

Un hallazgo cita el elemento, el criterio y qué falla. Sin captura o sin diseño no hay auditoría.

Source: WCAG 2.2. WCAG-EM del W3C para el método de evaluación. ARIA Authoring Practices Guide para un widget propio.

## Antes de escribir

1. Lee solo [design](references/design.md) o [implementation](references/implementation.md).

References: [design](references/design.md), [implementation](references/implementation.md).

## Entrega

Cada archivo de este skill va en `adrenaline/accessibility/`, o en `outputDirs["plugin-accessibility"]` si `.cursor/adrenaline.json` da una ruta relativa válida. Si `adrenaline/accessibility/` aún no existe y `accessibility/` en la raíz del proyecto ya tiene el `ORIGIN.json` o el `STATUS.md` de este plugin, sigue escribiendo ahí y dilo.

Si la persona nombra un proyecto, una app, un servicio o un dominio, el archivo de ese asunto va en `<subject>/`. Un archivo de todo el producto se queda en la raíz de la salida. `<NNN>` es el siguiente número libre en toda la carpeta. La celda `archivo` es `<subject>/<file>` cuando hay asunto (`doc/arch/adr-008-asunto-subcarpeta.md`).

Escribe `ORIGIN.json` junto a `STATUS.md` al crear la carpeta, y otra vez solo si falta o un campo difiere. Campos: `suite` `ADRenaline-Suite`, `plugin` `plugin-accessibility`, `repository` `https://github.com/ADRenaline-Suite/plugin-accessibility`, `convention` `adr-001`. No es un archivo `<NNN>` y no tiene fila en `STATUS.md`.

No inventes un dato que la persona no dio. Un título obligatorio sin dato queda como hueco y el archivo sigue `proposed`. "None." llena un título.

## Done

- [ ] Solo se aplicó la referencia de este command.
- [ ] La carpeta de salida, la subcarpeta del asunto, `ORIGIN.json` y `STATUS.md` coinciden con las reglas de entrega.
- [ ] Un dato obligatorio que falta es un hueco. El archivo sigue `proposed`.

## Example

Un pedido que nombra la pieza y su fuente escribe un archivo. Un pedido sin esa fuente no escribe nada y nombra el hueco.
