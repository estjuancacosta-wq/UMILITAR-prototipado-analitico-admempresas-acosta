# Hipótesis Registradas — Tablero de priorización

Tablero CRUD (crear, editar, eliminar) para gestionar las hipótesis de negocio del
proyecto, con comprobación de patrón/refutación y exportación a JSON. Sin backend:
todo se guarda en `localStorage` del navegador.

## Cómo publicarlo en GitHub Pages

1. Crea un repositorio nuevo (o usa uno existente) y sube el archivo `index.html`
   a la raíz (o a una carpeta `docs/` si prefieres).
2. En GitHub: **Settings → Pages → Build and deployment → Source**, elige
   `Deploy from a branch`, selecciona la rama `main` y la carpeta `/ (root)`
   (o `/docs` si lo pusiste ahí).
3. Guarda. GitHub te dará una URL tipo
   `https://<tu-usuario>.github.io/<tu-repo>/` en 1-2 minutos.

## Cómo correrlo en local

No necesita instalación ni servidor: abre `index.html` directamente en el
navegador (doble clic, o clic derecho → "Abrir con" tu navegador).

## Datos precargados

El tablero arranca con las 3 hipótesis del ejercicio (H-01, H-02, H-03),
tomadas del Tablero de priorización y su Ficha de Indicador:

- **H-01** — Plataforma digital colaborativa con producción bajo demanda
- **H-02** — Comunicación transparente de trazabilidad y valor
- **H-03** — Manufactura ágil + pauta digital hipersegmentada

## Funcionalidad

- **Filtros**: por Estado, Impacto, Fase DT, y búsqueda libre por texto.
- **Minimum Analytical Experiment**: ingresa el resultado medido y pulsa
  "Comprobar" — el tablero lo compara contra el patrón esperado y la condición
  de refutación de esa hipótesis, y marca el Estado (Verde/Amarillo/Rojo)
  automáticamente.
- **+ Nueva Hipótesis**: agrega registros nuevos desde un formulario modal.
- **✎ / 🗑**: editar o eliminar una hipótesis existente.
- **Exportar JSON**: descarga el estado actual de todas las hipótesis.

## Notas técnicas

- Un único archivo (`index.html`) con HTML, CSS y JS embebidos — no requiere
  build ni dependencias externas.
- Persistencia vía `localStorage` bajo la clave `hipotesis_registradas_v1`.
  Si alguna vez quieres reiniciar los datos de fábrica, borra esa clave desde
  las herramientas de desarrollador del navegador (Application → Local Storage).
- Responsive: en pantallas angostas, la tabla pasa a un layout de tarjetas.
