# Formulario de Delegados

Formulario web simple para registro de delegados con conexión a Google Sheets.

## 📋 Campos del formulario

- **Centro**: Campo de búsqueda con 85 centros disponibles
- **Correo electrónico**: Validación de formato de email
- **Nombre de pila**: Campo de texto

## 🚀 Despliegue

### Opción 1: Abrir directamente

Simplemente abre `index.html` en tu navegador.

### Opción 2: Servidor local

```bash
# Con Python
python -m http.server 8000

# Con Node.js
npx serve
```

Luego accede a `http://localhost:8000`

## 🔗 Conexión con Google Sheets

### 1. Crear el script

1. Abre tu Google Sheet
2. Ve a **Extensiones → Apps Script**
3. Copia el código de `apps-script.gs` y pégalo
4. Guarda el proyecto

### 2. Publicar

1. **Publicar → Deploy as web app**
2. Configura:
   - **Execute as**: Yo
   - **Who has access**: Cualquiera (anonymous)
3. Copia la URL del deployment

### 3. Conectar el formulario

Edita `index.html` y busca la línea:

```javascript
const SCRIPT_URL = 'https://script.google.com/macros/s/TU_SCRIPT_ID/exec';
```

Reemplaza la URL por la que obtuviste en el paso anterior.

## 📁 Archivos

```
delegados/
├── index.html       # Formulario principal
├── apps-script.gs   # Código para Google Sheets
└── README.md        # Este archivo
```

## ✅ Requisitos

- Navegador moderno (Chrome, Firefox, Safari, Edge)
- Cuenta de Google para Google Sheets