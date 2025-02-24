# 🚀 Combinador de Archivos CSV

![PowerShell](https://img.shields.io/badge/PowerShell-%235391FE.svg?style=for-the-badge&logo=powershell&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)

**Combinador de Archivos CSV** es un script en PowerShell diseñado para combinar múltiples archivos CSV en uno solo, manteniendo los encabezados únicos del primer archivo y omitiéndolos en los archivos subsiguientes. Este proyecto es ideal para tareas de auditoría, consolidación de datos y procesamiento de archivos grandes.

---

## 📋 Tabla de Contenidos
- [Descripción del Proyecto](#-descripción-del-proyecto)
- [Características](#-características)
- [Instalación](#-instalación)
- [Uso](#-uso)
- [Ejemplos](#-ejemplos)
- [Optimización y Consideraciones](#-optimización-y-consideraciones)
- [Contribución](#-contribución)
- [Licencia](#-licencia)
- [Créditos](#-créditos)

---

## 📝 Descripción del Proyecto

Este script está diseñado para combinar múltiples archivos CSV en un solo archivo maestro, optimizando el uso de memoria y garantizando que los encabezados no se dupliquen. Es especialmente útil para:

- Consolidar resultados de auditorías.
- Procesar grandes volúmenes de datos.
- Automatizar tareas repetitivas de combinación de archivos.

El script utiliza `StreamReader` y `StreamWriter` para procesar los archivos línea por línea, lo que lo hace eficiente incluso con archivos de gran tamaño.

---

## ✨ Características

- **Combina archivos CSV**: Fusiona múltiples archivos CSV en uno solo.
- **Encabezados únicos**: Mantiene los encabezados solo del primer archivo.
- **Eficiencia en memoria**: Procesa archivos línea por línea, ideal para grandes volúmenes de datos.
- **Manejo seguro de recursos**: Usa `try/finally` para garantizar que los archivos se cierren correctamente.
- **Fácil de usar**: Solo requiere configurar las rutas de entrada y salida.

---

## 🛠 Instalación

1. **Requisitos**:
   - PowerShell 5.1 o superior.
   - Acceso de lectura/escritura a las rutas especificadas.

2. **Clonar el repositorio**:
   ```bash
   git clone https://github.com/tu-usuario/combinador-csv.git
   cd combinador-csv
   ```

3. **Configurar rutas**:
   - Edita el script `combinar_csv.ps1` y actualiza las variables `$sourceFolder` y `$outputFile` con las rutas deseadas.

---

## � Uso

1. **Ejecutar el script**:
   Abre PowerShell y navega al directorio del proyecto. Luego, ejecuta:
   ```powershell
   .\combinar_csv.ps1
   ```

2. **Verificar la salida**:
   - El archivo combinado se guardará en la ruta especificada en `$outputFile`.
   - Se mostrará un mensaje en la consola indicando la ubicación del archivo combinado.

---

## 🧩 Ejemplos

### Estructura de archivos de entrada
- `archivo1.csv`:
  ```
  # Fecha de Ejecución: 2025-02-24 23:21:37
  Cliente,Servidor,Fecha de Ejecución,Usuario,Días Último Cambio,Fecha Último Cambio,Tipo Cuenta,Requiere Cambio,Fortaleza,Estado,Informe
  KIO,redhat-vm,24/02/2025 23:21,nobody,819,28/11/2022,Local,Sí,Cumple,rojo,ALERTA: Contraseña expirada (819 días).
  ```

- `archivo2.csv`:
  ```
  # Fecha de Ejecución: 2025-02-24 23:21:37
  Cliente,Servidor,Fecha de Ejecución,Usuario,Días Último Cambio,Fecha Último Cambio,Tipo Cuenta,Requiere Cambio,Fortaleza,Estado,Informe
  KIO,redhat-vm,24/02/2025 23:21,itan_flores,32,23/01/2025,Local,Sí,Cumple,rojo,ALERTA: Contraseña expirada (32 días).
  ```

### Archivo de salida combinado
- `master_password_audit.csv`:
  ```
  # Fecha de Ejecución: 2025-02-24 23:21:37
  Cliente,Servidor,Fecha de Ejecución,Usuario,Días Último Cambio,Fecha Último Cambio,Tipo Cuenta,Requiere Cambio,Fortaleza,Estado,Informe
  KIO,redhat-vm,24/02/2025 23:21,nobody,819,28/11/2022,Local,Sí,Cumple,rojo,ALERTA: Contraseña expirada (819 días).
  KIO,redhat-vm,24/02/2025 23:21,itan_flores,32,23/01/2025,Local,Sí,Cumple,rojo,ALERTA: Contraseña expirada (32 días).
  ```

---

## ⚙ Optimización y Consideraciones

- **Uso de memoria**: El script está optimizado para manejar archivos grandes procesándolos línea por línea.
- **Validación de datos**: Asegúrate de que todos los archivos CSV tengan la misma estructura para evitar inconsistencias.
- **Manejo de errores**: Considera agregar un bloque `catch` para manejar excepciones específicas, como archivos corruptos o acceso denegado.

---

## 🤝 Contribución

¡Las contribuciones son bienvenidas! Si deseas mejorar este proyecto, sigue estos pasos:

1. Haz un fork del repositorio.
2. Crea una rama con tu feature (`git checkout -b feature/nueva-funcionalidad`).
3. Realiza tus cambios y haz commit (`git commit -m 'Añadir nueva funcionalidad'`).
4. Haz push a la rama (`git push origin feature/nueva-funcionalidad`).
5. Abre un Pull Request.

---

## 📜 Licencia

Este proyecto está bajo la licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.

---

## 👏 Créditos

- **Autor**: [Tu Nombre](https://github.com/tu-usuario)
- **Inspiración**: Necesidad de automatizar la consolidación de archivos CSV.
- **Herramientas**: PowerShell, GitHub.

---

✨ **¡Gracias por usar este proyecto!** ✨
```

---

### **Características del README.md**
1. **Badges**: Usa badges para resaltar información clave (PowerShell, GitHub, Licencia).
2. **Tabla de Contenidos**: Facilita la navegación con enlaces a las secciones.
3. **Secciones claras**: Cada sección está bien definida y explicada.
4. **Formato limpio**: Usa Markdown avanzado para un diseño profesional.
5. **Instrucciones detalladas**: Incluye pasos claros para la instalación y el uso.
6. **Ejemplos prácticos**: Muestra cómo funciona el script con ejemplos de entrada y salida.
7. **Contribución y licencia**: Fomenta la colaboración y aclara los términos de uso.

Este `README.md` está listo para ser utilizado en tu repositorio de GitHub y proporciona una experiencia de usuario clara y profesional. ¡Espero que sea útil! 😊
