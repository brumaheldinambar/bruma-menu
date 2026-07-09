<p align="center">
  <img src="assets/brumi.svg" alt="Brumi" width="90">
</p>

<h1 align="center">BRUMA — Menú de Experiencias Líquidas</h1>

<p align="center">
  Menú interno de cócteles y mocktails del equipo Bruma, conectado a Airtable en tiempo real.<br>
  <em>Lo efímero, contenido.</em>
</p>

---

## ¿Qué es esto?

Un **live artifact de Claude Cowork**: una app HTML de un solo archivo ([`index.html`](index.html)) con CRUD completo del menú —cócteles y mocktails— que lee y escribe directamente en nuestra base de Airtable.

Funciones:

- **Fichas expandibles** con ingredientes, técnica, garnish, cristalería y puntuación (1–5 ★).
- **Filtros** por estilo (de autor / clásico), licor, categoría, perfil de sabor y nivel (Halo / Ámbar / En prueba).
- **Notas internas** por trago, guardadas en Airtable.
- **Crear, editar y eliminar** tragos con formulario validado.

## ⚠️ Cómo usarlo (importante)

Este archivo **no funciona como página web normal** (no basta con abrirlo en el navegador): usa el puente `window.cowork.callMcpTool` para hablar con Airtable, que solo existe dentro de **Claude Cowork**.

Para usarlo:

1. Descarga `index.html` de este repo.
2. Ábrelo como artifact en una sesión de **Claude Cowork** (arrástralo a la conversación o cópialo a tu carpeta de Artifacts).
3. Asegúrate de tener el **conector de Airtable** activo en Cowork, con acceso a la base *Bruma Menu*.
4. Al abrirse, el menú carga los tragos automáticamente. Cambios que guardes se escriben en Airtable para todo el equipo.

> Nota: el código contiene los IDs de la base y tablas de Airtable (no credenciales). El acceso real depende de que tu cuenta de Airtable tenga permiso sobre la base.

## Imagen de marca

La interfaz sigue **BRUMA · Foundations** en modo **HALO** (claro):

| Elemento | Token |
|---|---|
| Fondo | Cream 50 `#FDFBF6` |
| Superficies | Cream 100 `#F9F2E7` / Cream 200 `#F5E9DA` |
| Texto | Forest 900 `#0C1C17` / Cream 800 `#635643` |
| Acento | Amber 600 `#C87A2A` (texto/bordes) · Amber 500 `#D88E3F` (botones) |
| Verde | Sage 600 `#5E7256` |
| Peligro | Clay 700 `#934026` sobre Clay 50 `#FBEEE8` |
| Display | Croissant One |
| Cuerpo | Cabinet Grotesk (fallback: system-ui) |

Las fuentes se cargan de Google Fonts / Fontshare con fallbacks seguros: si el visor bloquea fuentes externas, la app sigue funcionando con Georgia / system-ui.

El logo **Brumi** ([`assets/brumi.svg`](assets/brumi.svg)) va incrustado inline en el header, recoloreado a Forest 700 para fondo claro.

## Editar el menú (datos)

Los datos **no viven en este repo** — viven en Airtable. Este repo solo versiona la interfaz. Para cambiar recetas, usa la app misma o Airtable directamente.
