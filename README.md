# OjoPrompt — Android (MVP)

OjoPrompt es una app Android (Kotlin + Jetpack Compose) para docentes que analiza fotos, videos y documentos para inferir prompts de IA y detectar contenido asistido por IA. Interfaz y resultados en español por defecto.

## 🚀 Cómo usar este repositorio

Este repositorio contiene un **script generador** que crea la estructura completa del proyecto Android. Puedes descargar el script y ejecutarlo localmente, o clonar este repositorio y usar el código como base.

### Opción 1: Usar el script generador (Recomendado para principiantes)

```bash
# 1. Descarga el script
wget https://raw.githubusercontent.com/nms20152009-netizen/ojoprompt-android/main/create_ojoprompt_repo.sh

# 2. Dale permisos de ejecución
chmod +x create_ojoprompt_repo.sh

# 3. Ejecuta el script
./create_ojoprompt_repo.sh

# 4. Descomprime el archivo generado
unzip ojoprompt-android.zip

# 5. Abre la carpeta 'app' con Android Studio
```

### Opción 2: Clonar directamente este repositorio

```bash
git clone https://github.com/nms20152009-netizen/ojoprompt-android.git
cd ojoprompt-android
```

## 📦 Estructura del Proyecto

```
ojoprompt-android/
├── app/                    # Proyecto Android (Kotlin)
│   ├── src/main/
│   │   ├── java/com/ojoprompt/
│   │   │   ├── app/        # MainActivity y UI principal
│   │   │   ├── ocr/        # Servicio OCR (ML Kit)
│   │   │   ├── analysis/   # Análisis local (TFLite)
│   │   │   └── backend/    # Cliente HTTP para backend
│   │   └── res/            # Recursos (layouts, strings, themes)
│   ├── build.gradle.kts    # Configuración del módulo
│   └── AndroidManifest.xml
├── backend/                # Backend opcional (FastAPI)
│   ├── app.py
│   └── requirements.txt
├── docs/                   # Documentación adicional
└── README.md
```

## 🛠️ Tecnologías Utilizadas

- **Kotlin** - Lenguaje principal
- **Jetpack Compose** - UI moderna y declarativa
- **CameraX** - Captura de fotos y videos
- **ML Kit** - OCR on-device (Text Recognition)
- **TensorFlow Lite** - Modelos de IA on-device
- **FastAPI** (Backend opcional) - Análisis en servidor

## 📝 Pasos de Desarrollo

### Para Desarrolladores Novatos:

1. **Configurar Android Studio**
   - Descargar Android Studio (versión más reciente)
   - Instalar SDK de Android 24+ (Nougat o superior)
   - Configurar emulador o conectar dispositivo físico

2. **Implementar Captura de Cámara**
   - Añadir dependencias de CameraX en `build.gradle.kts`
   - Solicitar permisos de cámara en runtime
   - Implementar vista previa y captura

3. **Integrar OCR On-Device**
   - Agregar ML Kit Text Recognition
   - Procesar imágenes capturadas
   - Extraer texto en español

4. **Análisis de Contenido**
   - Opción A: TFLite local para análisis básico
   - Opción B: Enviar a backend para análisis avanzado

5. **Interfaz en Español**
   - Todos los strings en `res/values/strings.xml`
   - Mensajes y resultados en español

## 🔒 Privacidad y Seguridad

- **Procesamiento Local**: Se recomienda OCR y análisis on-device siempre que sea posible
- **Consentimiento**: Solicitar siempre permiso antes de analizar trabajos de estudiantes
- **Datos Sensibles**: No almacenar contenido de estudiantes sin autorización
- **Backend Institucional**: Si se usa backend, debe ser institucional y seguro

## 🎯 Características Principales

- ✅ Captura de fotos y videos
- ✅ OCR en español (manuscritos y texto impreso)
- ✅ Extracción de frames de video
- ✅ Análisis de documentos PDF (próximamente)
- ✅ Inferencia de prompts de IA utilizados
- ✅ Detección de contenido generado por IA
- ✅ Interfaz completamente en español

## 📚 Recursos Adicionales

- [Documentación de Jetpack Compose](https://developer.android.com/jetpack/compose)
- [ML Kit Text Recognition](https://developers.google.com/ml-kit/vision/text-recognition)
- [CameraX](https://developer.android.com/training/camerax)
- [TensorFlow Lite](https://www.tensorflow.org/lite)

## 🤝 Contribuciones

Este es un proyecto educativo. Las contribuciones son bienvenidas:

1. Fork el repositorio
2. Crea una rama para tu feature (`git checkout -b feature/nueva-funcionalidad`)
3. Commit tus cambios (`git commit -m 'Añadir nueva funcionalidad'`)
4. Push a la rama (`git push origin feature/nueva-funcionalidad`)
5. Abre un Pull Request

## 📄 Licencia

MIT License - Ver archivo [LICENSE](LICENSE) para más detalles.

## 👨‍💻 Autor

Creado como proyecto educativo para docentes que desean entender y detectar el uso de IA en trabajos académicos.

## ⚠️ Nota Importante

Este repositorio contiene un **esqueleto básico** del proyecto. Es necesario completar la implementación siguiendo las instrucciones en los comentarios del código. El objetivo es que los desarrolladores aprendan implementando las funcionalidades paso a paso.

---

**¿Necesitas ayuda?** Abre un Issue en este repositorio con tus preguntas.
