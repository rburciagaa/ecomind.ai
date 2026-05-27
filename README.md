# EcoMind AI - Versión Web

Esta es la versión web de EcoMind AI, una aplicación de inteligencia artificial especializada en ecología y medio ambiente.

## ¿Qué cambió?

✅ **Antes (Tkinter Desktop):** Solo funcionaba en Windows/Mac/Linux  
✅ **Ahora (Web Flask):** Funciona en cualquier navegador (Desktop, Tablet, Móvil)

## Funcionalidades

- 🤖 Consultas a IA (Groq Llama 3.3 70B)
- 🎨 Generación de imágenes ecológicas
- 📄 Exportación a PDF
- 📊 Exportación a PowerPoint
- 📝 Exportación a TXT
- 📱 **Totalmente responsive (funciona en móviles)**

## Instalación

### 1. Requisitos
- Python 3.8+
- pip

### 2. Clonar/Descargar el proyecto

```bash
# Crear carpeta del proyecto
mkdir ecomind-ai
cd ecomind-ai

# Copiar los archivos
# - app.py (en la carpeta raíz)
# - templates/index.html (en subcarpeta templates)
```

### 3. Instalar dependencias

```bash
pip install flask flask-cors groq requests pillow pypdf python-pptx
```

### 4. Crear estructura de carpetas

```
ecomind-ai/
├── app.py
├── templates/
│   └── index.html
└── static/
    └── uploads/  (se crea automáticamente)
```

### 5. Ejecutar la aplicación

```bash
python app.py
```

La app estará disponible en: **http://localhost:5000**

## Cómo usar

1. **Abre el navegador** en `http://localhost:5000`
2. **Escribe una pregunta** sobre ecología
3. **Haz clic en "Preguntar IA"** para obtener respuesta
4. **Genera imágenes, PDF, PPT o TXT** con el resultado
5. **Descarga los archivos** directamente

## Diferencias con la versión Desktop

| Feature | Desktop (Tkinter) | Web (Flask) |
|---------|-------------------|------------|
| Plataforma | Solo escritorio | Cualquier navegador |
| Móvil | No | Sí (responsive) |
| Instalación | Compleja | Simple |
| Interfaz | UI personalizada | HTML/CSS moderna |
| Accesibilidad | Limitada | Excelente |
| Hospedaje | Local | Puede subirse a servidor |

## Características implementadas ✅

- ✅ Consultas a IA (Groq API)
- ✅ Generación de imágenes (Pollinations AI)
- ✅ Exportación a PDF
- ✅ Exportación a PowerPoint
- ✅ Exportación a TXT
- ✅ Interfaz responsive
- ✅ Loading states
- ✅ Mensajes de error/éxito
- ✅ Descarga de archivos

## Características NO implementadas

(Consideradas innecesarias en versión web)

- ❌ Video narrado (muy pesado en web, mejor hacerlo en backend)
- ❌ Análisis de archivos cargados (se puede agregar después)
- ❌ Búsqueda en Google Images/YouTube (abre en pestaña nueva)
- ❌ Animaciones 3D complejas (se pueden agregar con Canvas)

## Próximas mejoras posibles

- [ ] Agregar análisis de archivos PDF/PPTX cargados
- [ ] Mejorar animaciones con Canvas
- [ ] Agregar historial de consultas
- [ ] Sistema de temas claro/oscuro
- [ ] Hospedaje en servidor (Heroku, Railway, etc)

## Solucionar problemas

### Error "ModuleNotFoundError"
```bash
pip install flask flask-cors groq requests pillow pypdf python-pptx
```

### Error "GROQ_API_KEY no configurada"
Verifica que el archivo `app.py` tenga la API key correcta en:
```python
GROQ_API_KEY = "tu_api_key_de_groq_aqui"
```

### Error "Puerto 5000 en uso"
Cambiar el puerto en `app.py`:
```python
if __name__ == '__main__':
    app.run(debug=True, port=5001)  # Cambiar a otro puerto
```

### Imagen no se genera
- Revisar conexión a internet
- Intentar con otra descripción
- Los servidores de Pollinations a veces son lentos

## Para la alumna

Esta versión web es perfectamente funcional y lista para usar. Si necesita convertir a APK de verdad, siga estos pasos:

1. **Opción A:** Usar un servicio como **PWA (Progressive Web App)** para convertir el sitio a app móvil
2. **Opción B:** Usar **Tauri** para crear ejecutables de escritorio
3. **Opción C:** Reescribir con **Kivy** para APK nativo

## Autor

Convertido a web por: Claude AI  
Original: Alumna FIME  
Año: 2024-2025

---

**¿Preguntas?** Consulta el README o contacta al instructor.
