<p align="center">
  <img src="assets/brumi.svg" alt="Brumi" width="90">
</p>

<h1 align="center">BRUMA — Menú de Experiencias Líquidas</h1>

<p align="center">
  Menú interno de cócteles y mocktails del equipo Bruma, conectado a Airtable en tiempo real.<br>
  <em>Lo efímero, contenido.</em>
</p>

---

## 🍸 Úsalo aquí

### → **https://brumaheldinambar.github.io/bruma-menu/**

La primera vez te pedirá tu **token personal de Airtable** (se guarda solo en tu navegador, nunca sale de tu equipo). Para crearlo:

1. Entra a **[airtable.com/create/tokens](https://airtable.com/create/tokens)**.
2. Crea un token con los permisos (*scopes*) `data.records:read` y `data.records:write`.
3. En *Access*, selecciona la base del menú Bruma.
4. Copia el token (empieza con `pat…`) y pégalo en la pantalla de entrada del menú.

Necesitas ser **colaborador de la base de Airtable** — el token solo da el acceso que tu cuenta ya tiene. Para cambiar de token más adelante, usa el enlace "Cambiar token de Airtable" al pie de la página.

## ¿Qué es esto?

Una app HTML de un solo archivo ([`index.html`](index.html)) con CRUD completo del menú —cócteles y mocktails— que lee y escribe directamente en nuestra base de Airtable.

Funciones:

- **Fichas expandibles** con ingredientes, técnica, garnish, cristalería y puntuación (1–5 ★).
- **Filtros** por estilo (de autor / clásico), licor, categoría, perfil de sabor y nivel (Halo / Ámbar / En prueba).
- **Notas internas** por trago, guardadas en Airtable.
- **Crear, editar y eliminar** tragos con formulario validado.

Funciona en **modo dual**:

- **Navegador normal** (GitHub Pages o abriendo el archivo localmente): usa la API REST de Airtable con tu token personal.
- **Claude Cowork**: si se abre como live artifact, detecta el puente `window.cowork` y usa el conector MCP de Airtable automáticamente, sin token.

> Seguridad: este repo es público, pero **los datos no lo son**. El código solo contiene los IDs de la base y tablas de Airtable (no credenciales); recetas, notas y puntuaciones solo se ven con un token de una cuenta con permiso sobre la base.

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
