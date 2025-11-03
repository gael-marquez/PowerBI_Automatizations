# 📊 Manual de Automatización - Área de Cobranza

## 🎯 Descripción General

Este manual describe el proceso de automatización para la generación de reportes de cobranza utilizando Power Automate, SharePoint y Power BI. El flujo automatizado procesa datos judiciales y extrajudiciales para generar reportes consolidados.

---
## 🔄 Proceso de Automatización

### **Paso 1: Preparar el Archivo Bucket** 📁

1. Abrir la hoja **"Bucket"** en Excel
2. Seleccionar todos los datos: `Ctrl + *`
3. Ir a **Insertar → Tabla**
4. Asignar el nombre: `TablaF1`
5. Guardar el archivo como: `bucket.xlsx`

> 💡 **Tip:** Asegúrate de que todos los datos estén dentro del rango seleccionado antes de crear la tabla.

---

### **Paso 2: Preparar el Archivo de Reportes** 📝

#### Hoja Judicial:
1. Abrir la hoja **"Judicial"**
2. Seleccionar todos los datos: `Ctrl + *`
3. Ir a **Insertar → Tabla**
4. Asignar el nombre: `TablaJudicial`

#### Hoja Extrajudicial:
1. Abrir la hoja **"Extrajudicial"**
2. Seleccionar todos los datos: `Ctrl + *`
3. Ir a **Insertar → Tabla**
4. Asignar el nombre: `TablaExtrajudicial`

5. Renombrar el archivo siguiendo la nomenclatura: `Reportes.xlsx`

> ⚠️ **Importante:** Verifica que los nombres de las tablas sean exactos para evitar errores en la automatización.

---

### **Paso 3: Cargar Archivos a SharePoint** ☁️

#### Ubicación de los archivos:

| Archivo | Ruta en SharePoint |
|---------|-------------------|
| `bucket.xlsx` | `/Buckets/` |
| `reporte_[...].xlsx` | Raíz del sitio |

**URL Base:** [https://finansustentable.sharepoint.com/sites/Cobranza-Automatizaciones/Documentos](https://finansustentable.sharepoint.com/sites/Cobranza-Automatizaciones/Documentos)

---

### **Paso 4: Activación del Flujo** ⏳

Una vez cargados los archivos, el flujo de Power Automate se ejecutará automáticamente.

- ⏱️ **Tiempo de procesamiento:** Aproximadamente 5 minutos
- 📧 **Notificación:** Recibirás un correo electrónico con:
  - Reporte procesado adjunto
  - Link directo a Power BI

---

### **Paso 5: Acceder al Reporte en Power BI** 📈

1. Abrir el link de Power BI recibido por correo
2. Localizar la tabla de interés
3. Hacer clic en **"..."** (menú de opciones) debajo de la tabla
4. Seleccionar **"Exportar datos"**
5. Elegir **"Exportar"**

---

### **Paso 6: Consolidar Datos para el Día Siguiente** 🔄

1. Se descargarán dos diferentes archivos Excel (uno por tabla)
2. Consolidar todos los archivos en un solo Excel, cada tabla en una hoja diferente
3. Repetir los pasos del **Paso 2**:
   - Crear `TablaJudicial`
   - Crear `TablaExtrajudicial`
   - Renombrar apropiadamente
4. El archivo quedará listo para el cruce del día siguiente
---

## 📌 Notas Importantes

- ⚡ **No interrumpir el flujo:** Una vez cargados los archivos, espera a recibir la notificación por correo
- 🔄 **Nomenclatura consistente:** Mantén los nombres de tablas y archivos según lo especificado
- 💾 **Respaldos:** Conserva copias de los archivos originales antes de procesarlos

---

<div align="center">

**🚀 Automatización Power Automate | Área de Cobranza**

*Versión 1.0 - 2025*

</div>
