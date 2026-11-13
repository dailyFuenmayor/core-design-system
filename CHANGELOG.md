# Changelog

Historial del archivo de Figma de CORE. El proyecto sigue versionado semántico: mayor.menor.parche.

## v1.0 · Versión estable

**Agregado**
- Página License: CORE bajo CC BY 4.0 con atribución requerida y ejemplo, aclaración de que la licencia no cubre marcas, logos ni recursos de terceros, licencias de terceros (Lucide ISC, Feather MIT, Geist e IBM Plex SIL OFL 1.1) y aclaración de que Acme Projects y Nova son ficticios.
- Archive: registro de elementos retirados.
- Miniatura para Figma Community.

**Cambiado**
- Cover, Showcase, Getting started y Component guidelines actualizados a v1.0.
- Elevation: el ejemplo de foco muestra el anillo oficial `border/focus` y ya no usa un estilo de efecto.
- Estados de revisión: las páginas pasan a «Estable · v1.0».

**Retirado**
- Estilo de efecto `focus/ring`: ningún componente lo usaba. Los estilos de efecto pasan de 6 a 5 (`shadow/xs` a `shadow/xl`); `border/focus` es el único criterio de foco.
- Página Playground.

### v1.0.1 (archivo de trabajo)

- Color › Primitivos: el espaciado de la fila gris pasa de 12 a 8 px para que los 12 colores entren completos en el contenedor (gray/950 se veía recortado). Sin cambios en valores, nombres, variables ni referencias.

## v0.9.3

- Foco unificado con un anillo separado (capa Focus ring, `border/focus` + `border-width/strong`, 2 px de separación) en 17 componentes y 57 variantes.
- Component guidelines › 7 · Estado focus: criterio común, geometría, contraste en las 4 combinaciones y galería de foco en CORE y Nova, Light y Dark.
- Tabs/Trigger y SidebarNav/Item dejan de usar una sombra de color fijo.

## v0.9.2

- Template SaaS Dashboard en CORE y Nova, Light y Dark.
- Card outlined: el borde pasa de `border/subtle` a `border/default`.
- Tag y Calendar/Day: foco con anillo separado de 2 px.

## v0.9.1

- Estado focus en DropdownMenu/Item, Tag, Breadcrumb/Item, Pagination/Item, Table/HeaderCell y Calendar/Day.
- Toast: propiedad `dismissible`.

## v0.8.0

- Stat, PageHeader, AppShell y DatePicker (con Calendar y Calendar/Day).
- Caso Acme actualizado con AppShell, PageHeader, Stat y DatePicker.
- Revisión: 39 componentes, 191 variables, 0 referencias rotas, 0 colores sin token, 92 pares de contraste comprobados en 4 combinaciones de marca y tema.

## v0.7.0

- Caso práctico Acme Projects: 17 pantallas en Light, 17 en Dark y 10 con la marca Nova; prototipo con 7 flujos.
- Segunda marca Nova como modo de la colección `brand` (escala violeta e IBM Plex). Total: 191 variables.

## v0.6.0

- EmptyState.
- Patterns: Autenticación, Formularios y validación, Estados vacíos, Búsqueda y filtros, Manejo de errores.

## v0.5.0

- Tag, Accordion/Item, ProgressBar y Skeleton.

## v0.4.0

- Feedback: Alert, Toast, Tooltip y Spinner. Data display: Avatar, Card y celdas de tabla. Navigation: Tabs, Breadcrumb, Pagination y SidebarNav. Overlays: DropdownMenu y Dialog.

## v0.3.0

- Forms: TextField, Textarea, Select. Selection: Checkbox, Radio y Switch.

## v0.2.0

- Grid y layout, 50 iconos de Lucide, Button, IconButton y Badge.

## v0.1.0

- Estructura de páginas, variables (primitives, brand, theme y dimension), 13 estilos de texto en Geist y Geist Mono, estilos de sombra y documentación de foundations.
