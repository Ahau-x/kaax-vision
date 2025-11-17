# Kaax Vision – QGIS Plugin (Versión Alpha) #

Kaax Vision es un plugin experimental desarrollado por **Ahau-x** para integrar el poder de la visión computarizada directamente en QGIS. Permite segmentar ortomosaicos utilizando modelos de **SAM 2 (Segment Anything Model 2)** y facilita la conexión con la plataforma **Kaax** para entrenamiento y carga de modelos personalizados.

---

## ⚙️ Instalación del Plugin ⚙️

### 0️⃣ Descargar el Plugin
Descarga el archivo ZIP del plugin (**kaax_vision.zip**) desde el siguiente enlace:
https://drive.usercontent.google.com/download?id=1LeYtAjM_7TxIvx50gNfbJNcHuBxiMXj_&export=download&authuser=0&confirm=t&uuid=bebb2dc3-e8c5-4b2c-ab38-a20695a44fef&at=ALWLOp7OtOpQr_GvUB9W5NMigo1k:1763410471153

### 1️⃣ Requisitos previos
- Tener instalada una versión de **QGIS 3.34 (LTR)** o superior.
- Contar con conexión a Internet durante la instalación inicial (solo la primera vez).

---

### 2️⃣ Instalación del ZIP en QGIS

1. Abre **QGIS**.
2. Ve a:
   **Complementos -> Administrar e instalar complementos -> Instalar desde un ZIP**
3. Selecciona el archivo **`kaax_vision.zip`** que descargaste.
4. Presiona **“Instalar complemento”**.
5. QGIS mostrará un mensaje indicando que se instalarán las dependencias necesarias.
   > El plugin se cerrará automáticamente, descargará e instalará PyTorch, Hydra, Omegaconf, PyShp y Geopandas, y luego reiniciará QGIS.
6. Una vez completado el proceso, vuelve a abrir QGIS y el plugin estará listo para usar.

---

### ⚠️ Si ocurre un error durante la instalación

Si por algún motivo la instalación automática de dependencias falla o el plugin no se inicia correctamente, puedes instalar las dependencias manualmente:

1. Abre la carpeta donde QGIS guarda los plugins:
   C:\Users\<TU_USUARIO>\AppData\Roaming\QGIS\QGIS3\profiles\default\python\plugins\
2. Entra a la carpeta:
   kaax_vision
3. Ejecuta (doble click) el script:
   install_deps.py
4. Espera a que aparezca el mensaje **“✅ Instalación completada correctamente”**
5. Reinicia QGIS manualmente.

---

## 🔐 Inicio de Sesión en Kaax 🔐

Antes de utilizar el plugin, debes **iniciar sesión con tu cuenta Kaax**:

1. Abre el panel **Kaax Vision** dentro de QGIS.
2. Ingresa tus credenciales de Kaax.
- Si aún no tienes cuenta, puedes registrarte gratis en:
  👉 https://www.kaax-agritech.com/es/signup

El inicio de sesión es gratuito y te permite usar los modelos base de segmentación.

---

## 🧩 Funcionalidades Principales 🧩

### 🧠 Segmentación con SAM 2

Kaax Vision incluye el modelo base de **SAM 2 (Segment Anything Model 2)**, que permite segmentar ortomosaicos de dos formas:

#### 1️⃣ Segmentar Todo
Divide el ortomosaico en *tiles* (bloques) y segmenta toda la imagen automáticamente.
Solo define el tamaño del *tile* y presiona **“Segmentar Todo”**.

#### 2️⃣ Segmentar con Click
Permite hacer click directamente sobre el área a segmentar.
El modelo generará una máscara alrededor del área seleccionada.
> Si el modelo no reconoce un objeto en la zona clickeada, no generará ninguna máscara.

---

### 🧰 Cargar Modelos Personalizados

Por ahora, los modelos personalizados pueden **entrenarse y cargarse a través de la plataforma Kaax**.
Si deseas hacer un **fine-tuning del modelo SAM 2**, puedes seguir esta guía de Roboflow:
👉 https://blog.roboflow.com/fine-tune-sam-2-1/

> ⚙️ Para integrar tu modelo personalizado dentro del plugin, contáctanos directamente a través de **Ahau-x** para recibir apoyo técnico.

---

## 🚀 Uso Básico del Plugin 🚀

1. Inicia sesión con tu cuenta Kaax.
2. Carga la capa (ortomosaico o raster) que deseas segmentar.
3. Si no aparece, presiona **“Actualizar Capas”**.
4. Selecciona el modelo (por defecto: **SAM 2 Base**).
5. Elige el modo de segmentación:
- **Segmentar Todo**, o
- **Segmentar con Click**
6. Visualiza los polígonos resultantes directamente en QGIS.

---

## 🧪 Estado del Proyecto 🧪

> ⚠️ **Kaax Vision** es una versión **Alpha (Experimental)**.
Puede contener errores o limitaciones mientras se continúa desarrollando.
Se recomienda usarlo con fines de prueba, validación de modelos o exploración técnica.

Si deseas contribuir, reportar errores o solicitar soporte para integraciones avanzadas (entrenamiento, nuevos modelos o pipelines de inferencia), puedes contactar directamente a:

**Ahau-x – Unidad de Innovación Agrícola de Bitcode Group S.A.**
🌐 www.kaax-agritech.com

---

### 📄 Licencia

Kaax Vision © 2025 Ahau-x by Bitcode Group S.A.
Distribuido bajo licencia **propietaria experimental (Alpha)**.
El uso, redistribución o entrenamiento de modelos externos debe contar con autorización directa de Ahau-x.
