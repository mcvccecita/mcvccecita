# Image Management System for COVID-19 Dataset

Este sistema de gestión de imágenes está diseñado para facilitar el manejo eficiente de imágenes médicas en el conjunto de datos COVID-19 Radiography Database. A continuación, se describen las características y el uso del código.

## Características Principales

- **Gestión de Imágenes:** Permite agregar, actualizar y eliminar imágenes del conjunto de datos.
- **Modularización en Python:** Utiliza programación modular para mantener una estructura de código organizada.
- **Integración de Herramientas:** Implementa Pandas, Numpy y programación orientada a objetos.
- **Versionamiento de Código y Datos:** Proporciona seguimiento y control de versiones para facilitar la trazabilidad.
- **Buenas Prácticas:** Incluye documentación detallada y pruebas para garantizar la robustez del código.

## Uso del Código

1. **Configuración Inicial:**
   - Asegúrate de tener instaladas las bibliotecas necesarias: Pandas, Pillow (PIL), y tkinter.
   - Reemplaza la ruta de las imágenes en `image_path` con la ubicación real de tus archivos de imágenes.

2. **Ejecución:**
   - Ejecuta el script proporcionando la ruta del conjunto de datos como argumento (`dataset_path`).

3. **Interfaz Gráfica:**
   - La ventana principal muestra un visor de imágenes con botones de navegación ("Anterior" y "Siguiente").
   - La información de la imagen actual se presenta en una etiqueta debajo del visor.

4. **Funciones Adicionales:**
   - `add_image`: Agrega una nueva imagen al conjunto de datos.
   - `update_metadata`: Actualiza la información de metadatos de una imagen existente.
   - `delete_image`: Elimina una imagen y sus metadatos del conjunto de datos.
   - `get_image_metadata`: Obtiene los metadatos de una imagen específica.

## Ejemplo de Uso

```python
# Uso del programa
dataset_path = 'Viral Pneumonia.metadata.xlsx'
manager = ImageManager(dataset_path)

# Crear la ventana principal
root = Tk()
root.title("Image Viewer")

# Crear el visor de imágenes
viewer = ImageViewer(root, manager)

# Iniciar el bucle principal de la interfaz gráfica
root.mainloop()
