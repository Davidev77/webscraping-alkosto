# Web Scraping de Alkosto

Script de web scraping con Selenium para extraer información de productos del sitio e-commerce de Alkosto. Este proyecto extrae el nombre, precio e imagen de los productos disponibles relacionados con la palabra 'celulares' en la tienda online de Alkosto.

## Características

- **Carga dinámica automática**: Simula clics en el botón "Mostrar más" para cargar todos los productos disponibles (la página muestra inicialmente solo 25 productos por carga)
- **Extracción de datos**: Captura título, precio e imagen de cada producto
- **Exportación a CSV**: Guarda los datos en un archivo estructurado para análisis posterior

## Instalación

### 1. Crear entorno virtual (Recomendado)

Es recomendable crear un entorno virtual para evitar conflictos con las dependencias de otros proyectos:
```
python -m venv venv
```

### 2. Activar el entorno virtual

**En Windows (PowerShell):**
```
.venv\Scripts\Activate.ps1
```

**En Windows (CMD):**
```
.venv\Scripts\activate.bat
```

**En Linux/Mac:**
```
source venv/bin/activate
```

### 3. Instalar dependencias
```
pip install jupyterlab
pip install selenium
pip install pandas
```

O usando el archivo `requirements.txt`:
```
pip install -r requirements.txt
```
## Configuración

- La URL de Alkosto ya está configurada en el código, pero puedes modificarla según la categoría que desees scrapear, yo busqué 'celulares' pero tu puedes buscar cualquier otro producto

## Notas técnicas

- El script utiliza JavaScript para hacer clic en el botón "Mostrar más" y evitar problemas con elementos que puedan bloquear la interacción
- Incluye manejo de excepciones para detener el bucle cuando no hay más productos por cargar
- Los datos se exportan automáticamente a `productos.csv` al finalizar la extracción

## Estructura del CSV generado

| Columna | Descripción |
|---------|-------------|
| Título  | Nombre del producto |
| Precio  | Precio en formato texto |
| Imagen  | URL de la imagen del producto |

---
