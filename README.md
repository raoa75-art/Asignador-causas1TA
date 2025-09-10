# Asignador de Causas – Tribunal Ambiental (vista web)

Aplicación estática (un solo `index.html`) para **asignar causas** entre funcionarios según **carga ponderada** y visualizar el estado en **tablas y gráficos**.

## Demo
- GitHub Pages: `https://TU-USUARIO.github.io/asignador-ambiental/`  <!-- Reemplazar -->

## Características
- **Algoritmo Greedy lexicográfico**:
  - Prioriza **menor carga ponderada** `L = i·A + j·B + k·C`.
  - **No repite** el último funcionario si hay alternativa.
  - Desempate por **aptitud requerida** (A/B/C) *sin penalizar* la carga; si persiste, **azar**.
- **Capacidad máxima** por funcionario (editable; por defecto 20).
- **Estado inicial editable** (3 funcionarios).
- **Visualizaciones**:
  - Visualizador de cargas (A/B/C apilado).
  - **Inicial vs Actual** (totales).
  - **Distribución de aptitud** (sesión).
  - **Historial** de asignaciones (sesión).
- **Exportación CSV**: estado y log de eventos.

## Cómo usar
1. Abre `index.html` en un navegador moderno (Chrome/Edge/Firefox).
2. En “Asignación en línea”, elige **tipo de causa** (A/B/C) y **aptitud requerida** (A/B/C).
3. Pulsa **Asignar 1 causa**. Todo se actualiza: tablas, gráficos e historial.
4. Usa **Deshacer** para revertir la última asignación.
5. **Capacidades** y **ponderaciones** son editables (se reflejan en el cálculo y visualización).

> Nota: Los nombres de funcionarios se pueden editar en el archivo si lo requieres. Si el repo es público, considera usar nombres genéricos por privacidad.

## Despliegue en GitHub Pages
1. Sube `index.html` a un repo público.
2. En **Settings → Pages**: “Deploy from a branch”, selecciona **main** y **/(root)**.
3. La página quedará disponible en `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/`.

## Estructura
