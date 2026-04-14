# Sales Performance Dashboard - sales.io

**Dashboard interactivo de análisis de desempeño de ventas** con visualización de métricas clave, márgenes por producto y eficiencia operativa por región.

## 🎯 Descripción

Herramienta de análisis ejecutivo que consolida datos de ventas (enero-septiembre 2025) en un único panel interactivo con:

- **4 KPIs principales:** Ingresos totales, ganancia bruta, unidades vendidas, ticket promedio
- **Gráficos avanzados:** Evolución temporal (líneas), distribución por canal (dona), ingresos por región (barras)
- **Análisis de márgenes:** Rentabilidad por categoría de producto
- **Comparativas:** Ingreso vs. costo por categoría y análisis de eficiencia regional
- **Filtrado dinámico:** Análisis por región (Norte, Sur, Este, Oeste)

## 📊 Características

✅ 22 transacciones consolidadas  
✅ 4 zonas geográficas analizadas  
✅ 3 categorías de producto (Electrónica, Hogar, Ropa)  
✅ 2 canales de venta (En línea, Presencial)  
✅ Gráficos responsivos con Chart.js 4.4.1  
✅ Tema dark mode profesional  
✅ Filtros interactivos  

## 🚀 Acceso

**Versión publicada:** [https://gabrieltapia.github.io/sales.io/](https://gabrieltapia.github.io/sales.io/)
*Próximamente en GitHub Pages*

## 💻 Uso Local

Solo necesitas abrir el archivo `index.html` en cualquier navegador moderno. No requiere instalación ni dependencias locales.

```bash
# Opción 1: Doble clic en index.html
# Opción 2: Desde terminal
open index.html  # macOS
start index.html # Windows
xdg-open index.html # Linux
```

## 📦 Tecnologías

- **HTML5** — Estructura semántica
- **CSS3** — Temas variables, animaciones, grid responsive
- **JavaScript ES6+** — Lógica de filtrado y actualización de datos
- **Chart.js 4.4.1** — Visualización de gráficos (CDN)
- **Google Fonts** — DM Mono, Syne, Inter (CDN)

## 📈 Estructura de Datos

Archivo `index.html` incluye array `rawData` con 22 registros de transacciones:

```javascript
{
  fecha: 'DD/MM/YYYY',
  region: 'Norte|Sur|Este|Oeste',
  producto: 'Electrónica|Artículos del hogar|Ropa',
  canal: 'En línea|Presencial',
  unidades: number,
  precio: number,
  ingreso: number,
  costo: number,
  ganancia: number
}
```

## 🎨 Diseño

**Paleta de colores:**
- Cyan (#00e5ff) — Ingresos, primario
- Rose (#ff4d6d) — Ganancias, costos
- Yellow (#ffe600) — Acentos
- Purple (#7c3aed) — Énfasis
- Emerald (#00c896) — Éxito/Eficiencia
- Orange (#ff8c00) — Advertencia

## 🔧 Instalación en GitHub Pages

### Paso 1: Crear repositorio en GitHub
1. Ve a [github.com](https://github.com)
2. Crea un nuevo repositorio público llamado `sales.io`
3. **NO** inicialices con README/gitignore

### Paso 2: Inicializar Git localmente
```bash
cd sales.io
git init
git config user.name "Tu Nombre"
git config user.email "tu.email@example.com"
git add .
git commit -m "Initial commit: Sales dashboard"
git branch -m main  # Si está en master
```

### Paso 3: Conectar y publicar
```bash
git remote add origin https://github.com/tu-usuario/sales.io.git
git push -u origin main
```

### Paso 4: Activar GitHub Pages
1. En tu repo → **Settings** → **Pages**
2. Source: `Deploy from a branch`
3. Branch: `main` / `(root)`
4. **Save** → Espera 1-2 minutos
5. Tu sitio estará en: `https://tu-usuario.github.io/sales.io/`

## 📝 Actualización de Datos

Para cambiar los datos del análisis, edita el array `rawData` en `index.html` (línea ~430):

```javascript
const rawData = [
  { fecha: '15/1/2025', region: 'Norte', ... },
  // Agrega o modifica registros aquí
];
```

Los gráficos se regenerarán automáticamente.

## 🐛 Troubleshooting

**¿Los gráficos no cargan?**
- Verifica conexión a internet (necesita CDN para Chart.js)
- Abre consola (F12) y busca errores CORS

**¿GitHub Pages no publica?**
- Asegúrate que `index.html` está en la raíz
- El repo debe ser público
- Espera 2-3 minutos después del push

**¿Los estilos se ven roto?**
- Limpia caché del navegador (Ctrl+Shift+Del)
- Intenta en navegador diferente

## 📄 Licencia

Libre para uso personal y comercial.

## 👤 Autor

Creado: **Abril 2026**  
Base de datos: Enero-Septiembre 2025

---

**¿Preguntas o mejoras?** Edita este archivo o crea un issue en GitHub.
