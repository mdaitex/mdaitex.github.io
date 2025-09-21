# Repository Guidelines

## Project Structure & Module Organization
The project is intentionally lightweight: all runtime code lives at the repository root. `index.js` exposes the async `pandoc(args, input, base64Wasm)` bridge that boots the WASI runtime in the browser. `pandoc.js` is the bundled helper used in offline or Node-like environments that need CRC and gzip utilities. `pandoc.b64` and `pandoc.b64.gz` store the WebAssembly binary in plain and gzipped base64, while `mdlatex.html` and `mdlatexca.md` demonstrate Markdown-to-LaTeX flows. Long-form usage notes are collected in `uso_local_pandoc.md`.

## Build, Test, and Development Commands
No build step is required; serve the folder statically and the browser will load the assets. Typical loops are:
- `python -m http.server 8000` — quick local web server to test `mdlatex.html`.
- `gzip -dc pandoc.b64.gz > pandoc.b64` — regenerate the plain base64 version when updating the WASM blob.
- `gzip -c pandoc.wasm | base64 -w0 > pandoc.b64.gz` — refresh the gzipped asset from an upstream `pandoc.wasm`.

## Coding Style & Naming Conventions
Use modern ES modules, two-space indentation, and trailing commas for multiline literals. Favor camelCase for functions and variables, ALL_CAPS for shared constants, and descriptive file names in lowercase. When touching bundled files, document the build command that produced them.

## Testing Guidelines
There is no automated harness yet. Validate changes manually by converting a representative Markdown sample through `pandoc()` in the browser console and confirming the expected output (DOCX, ODT, LaTeX). When updating the WASM blob, verify the CRC matches the source artifact and load the demo page in at least Chrome and Firefox.

## Commit & Pull Request Guidelines
Adopt a concise `type: summary` commit style (e.g., `feat: add odt shortcut`). Include doc updates whenever behavior changes, especially for `uso_local_pandoc.md`. Pull requests should describe the conversion scenarios exercised, mention regenerated assets, and attach screenshots or sample files when UI output changes.

## Asset Handling & Security
Treat `pandoc.b64*` as source-of-truth binaries; avoid checking large temporary artifacts into version control. Never expose local API keys in example code. Keep demo pages free of third-party scripts so the offline promise remains intact.

## Operational Constraints
- No modificar la lógica de exportación (DOCX, ODT, HTML, LaTeX) sin aprobación explícita del responsable del proyecto; cambios no autorizados pueden provocar fallos graves en producción.
- No publicar pushes ni releases en GitHub sin consentimiento expreso previo.

## Localization
- Todas las cadenas de interfaz residen en `locales/<código>/translation.json` (formato i18next). Mantén las claves sincronizadas entre idiomas y evita cadenas sueltas en el HTML.
- Los textos de ayuda inicial se sirven desde archivos Markdown específicos por idioma (`mdlatex*.md`). Si añades un idioma nuevo, crea también su archivo de ayuda y enlázalo en `HELP_FILES` dentro de `index.html`.
