# Tokens de diseño

Exportación de las variables y estilos del archivo maestro de Figma de CORE (v1.0) al [formato DTCG](https://www.designtokens.org/tr/2025.10/format/) (Design Tokens Community Group, versión 2025.10).

**Licencia:** estos archivos son materiales propios de CORE y se distribuyen bajo [CC BY 4.0](../LICENSE). Si los usas o los transformas (por ejemplo, para generar CSS), indica la autoría y la licencia como se explica en [NOTICE.md](../NOTICE.md). Los nombres de familias tipográficas que contienen (Geist, IBM Plex) solo nombran fuentes de terceros: los archivos de fuentes no se incluyen y tienen su propia licencia.

Estos archivos son datos, no una librería: no incluyen código ni un paso de compilación. Puedes usarlos con herramientas compatibles con DTCG, como Style Dictionary o Tokens Studio, para generar CSS, JS u otros formatos.

## Archivos

| Archivo | Origen en Figma | Tokens |
|---|---|---|
| `primitives.tokens.json` | Colección `primitives` · modo Value | 75 |
| `brand.core.tokens.json` | Colección `brand` · modo CORE | 13 |
| `brand.nova.tokens.json` | Colección `brand` · modo Nova | 13 |
| `theme.light.tokens.json` | Colección `theme` · modo Light | 52 |
| `theme.dark.tokens.json` | Colección `theme` · modo Dark | 52 |
| `dimension.tokens.json` | Colección `dimension` · modo Default | 51 |
| `typography.tokens.json` | 13 estilos de texto | 13 |
| `shadow.tokens.json` | 5 estilos de efecto | 5 |
| `manifest.json` | Resumen: colecciones, modos, conteos y combinaciones | — |

Total de variables: **191** (75 + 13 + 52 + 51). Los estilos de texto y sombra son estilos de Figma, no variables, y se exportan aparte.

## Cómo se combinan

Cada archivo de modo usa los mismos nombres, así que para resolver una combinación se carga **un archivo de cada colección**:

| Combinación | Archivos |
|---|---|
| CORE · Light | `primitives` + `brand.core` + `theme.light` + `dimension` |
| CORE · Dark | `primitives` + `brand.core` + `theme.dark` + `dimension` |
| Nova · Light | `primitives` + `brand.nova` + `theme.light` + `dimension` |
| Nova · Dark | `primitives` + `brand.nova` + `theme.dark` + `dimension` |

`typography.tokens.json` referencia `{brand.font.sans}` y `{brand.font.mono}`, así que también se resuelve con el archivo de marca.

## Formato

- Los grupos siguen los nombres de Figma: `bg/action/primary` → `bg.action.primary`.
- Los alias de Figma se exportan como referencias DTCG: `"$value": "{brand.accent.600}"`.
- Colores: objeto DTCG con `colorSpace: "srgb"`, `components` (0–1, redondeados a 4 decimales), `hex` y `alpha` cuando es menor que 1.
- Medidas: `dimension` en `px`. Las columnas de grid (`grid.columns.*`) son `number`.
- Tipografía: `lineHeight` como proporción (por ejemplo 56/48 = 1,1667) y `letterSpacing` en px; los valores originales de Figma (px y %) se conservan en `$extensions`.
- `$description` conserva la descripción de cada variable en Figma.
- `$extensions["com.coredesignsystem"].figma` indica colección, nombre original de la variable y alcances (scopes).

## Verificación

Antes de publicar se comprobó:

- 191 variables exportadas: 75 · 13 · 52 · 51, igual que en el archivo de Figma.
- Las cuatro combinaciones resuelven todas sus referencias: 0 referencias rotas y 0 nombres duplicados.
- Cada referencia apunta a un token del mismo tipo.
- Los colores coinciden con los valores HEX documentados en Figma.

## Nombres en código

Convención usada en la documentación de CORE: `bg/action/primary` → `--core-bg-action-primary`.
