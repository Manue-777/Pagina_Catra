# 📋 Guía del Administrador - Sistema CATRA

## ¿Cómo agregar nuevas constancias o instructores?

El sistema ahora está conectado a **Google Sheets**. Ya **NO es necesario editar archivos de código**. Solo debes agregar datos en las hojas de cálculo.

---

## 📊 PASO 1: Agregar una Nueva Constancia

### 1. Abre la hoja de Constancias:
- Ve a Google Sheets y busca la hoja llamada **"CATRA - Constancias"**
- O usa este enlace: [Tu enlace de edición aquí]

### 2. Agrega una nueva fila con los siguientes datos:

| Columna | Descripción | Ejemplo |
|---------|-------------|---------|
| **Folio** | Número único de la constancia | CATRA-2025-00147125 |
| **Nombre** | Nombre completo del participante | JUAN PÉREZ GARCÍA |
| **Curp** | CURP del participante | PEGJ850505HDFRRN01 |
| **Curso** | Nombre del curso | MANEJO DE MONTACARGAS |
| **Duracion** | Duración del curso | 40 HORAS |
| **Calificacion** | Calificación obtenida | 9.5 / 10.0 |
| **Fecha** | Fecha de emisión | 15 DE OCTUBRE DE 2025 |
| **Instructor Id** | ID del instructor (debe existir) | inst001 |

**⚠️ IMPORTANTE:** La columna **"Instructor Id"** debe contener el ID exacto de un instructor que exista en la hoja de Instructores. Este enlace permite que el botón "Validación Oficial" lleve al perfil del instructor.

### 3. Guarda el documento
- Los cambios se guardan automáticamente en Google Sheets
- **El sitio web se actualizará automáticamente** (puede tardar unos segundos)

---

## 👨‍🏫 PASO 2: Agregar un Nuevo Instructor

### 1. Abre la hoja de Instructores:
- Ve a Google Sheets y busca la hoja llamada **"CATRA - Instructores"**
- O usa este enlace: [Tu enlace de edición aquí]

### 2. Agrega una nueva fila con los siguientes datos:

| Columna | Descripción | Ejemplo |
|---------|-------------|---------|
| **ID** | Identificador único del instructor | inst002 |
| **Nombre** | Nombre completo | Dr. Carlos Ramírez |
| **Especialidad** | Especialidad o profesión | Ingeniero Industrial |
| **CURP** | CURP del instructor | RAIC750315HDFRRL09 |
| **Resumen** | Descripción profesional | Ingeniero con 20 años de experiencia... |
| **Cedulas** | Cédulas separadas por \| | Cédula profesional 123456\|Maestría en Seguridad Industrial |
| **CV PDF** | Ruta al archivo PDF del CV (RECOMENDADO) | ../Images/CVs/Carlos/CV_Carlos.pdf |
| **CV Paginas** | Rutas de imágenes del CV separadas por \| (alternativa al PDF) | ../Images/CVs/Carlos/CV1.jpg\|../Images/CVs/Carlos/CV2.jpg |
| **Certificaciones** | Lista de certificaciones separadas por \| | Certificado ISO 9001\|Instructor STPS\|Evaluador CONOCER |

**💡 NUEVO:** Ahora puedes usar **un solo archivo PDF** en lugar de múltiples imágenes para el CV.

### 3. IMPORTANTE: Separador de listas
- Cuando una columna contiene **múltiples elementos** (certificaciones, páginas del CV, cédulas), usa el símbolo **`|`** (pipe) para separarlos
- Ejemplo: `Certificado 1|Certificado 2|Certificado 3`

### 4. Guarda el documento
- Los cambios se guardan automáticamente
- **El sitio web se actualizará automáticamente**

---

## 🖼️ PASO 3: Subir CV del Instructor

Ahora tienes **dos opciones** para subir el CV:

### **Opción A: Usar PDF (RECOMENDADO) 📄**

1. **Crea una carpeta** para el instructor en: `Images/CVs/NombreInstructor/`
2. **Sube el archivo PDF** del CV completo (ejemplo: `CV_Carlos.pdf`)
3. **En Google Sheets**, en la columna `CV PDF`, escribe la ruta:
   ```
   ../Images/CVs/NombreInstructor/CV_Carlos.pdf
   ```
4. **Deja vacía** la columna `CV Paginas`

**Ventajas:**
- ✅ **Un solo archivo** (más fácil de gestionar)
- ✅ **Mejor calidad** (texto seleccionable)
- ✅ **Más rápido** de cargar
- ✅ **Más profesional**

### **Opción B: Usar Imágenes (Alternativa) 🖼️**

1. **Crea una carpeta** para el instructor en: `Images/CVs/NombreInstructor/`
2. **Sube las imágenes** del CV (CV1.jpg, CV2.jpg, CV3.jpg, etc.)
3. **En Google Sheets**, en la columna `CV Paginas`, escribe las rutas separadas por `|`:
   ```
   ../Images/CVs/NombreInstructor/CV1.jpg|../Images/CVs/NombreInstructor/CV2.jpg|../Images/CVs/NombreInstructor/CV3.jpg
   ```
4. **Deja vacía** la columna `CV PDF`

**Nota:** Si ambas columnas tienen datos, el sistema usará el PDF por prioridad.

---

## ✅ Verificación

### Para verificar que todo funciona:

1. **Constancias**: Abre en el navegador:
   ```
   https://Manue-777.github.io/Pagina_Catra/index.html?folio=CATRA-2025-00147123
   ```
   (Reemplaza el folio con uno de tu hoja)

2. **Instructores**: Abre en el navegador:
   ```
   https://Manue-777.github.io/Pagina_Catra/instructor.html?id=inst001
   ```
   (Reemplaza el ID con uno de tu hoja)

---

## 🚨 Solución de Problemas

### ❌ "El folio no fue encontrado"
- Verifica que el folio esté escrito **exactamente igual** en Google Sheets
- Asegúrate de que la hoja esté **publicada en la web**

### ❌ "Instructor no encontrado"
- Verifica que el ID esté escrito **exactamente igual** en Google Sheets
- Asegúrate de que la hoja esté **publicada en la web**

### ❌ "Los datos no se actualizan"
- Espera unos segundos (puede haber un pequeño retraso)
- Refresca la página con **Ctrl+F5** (recarga forzada)
- Verifica que las hojas estén publicadas correctamente

---

## 🎯 PASO 4: Generar Códigos QR para las Constancias

### ¿Para qué sirve?
El generador de QR crea códigos QR que enlazan directamente a la verificación online de cada constancia. Puedes imprimir estos QR en las constancias físicas.

### Cómo Acceder:
**URL del Generador:**
```
https://Manue-777.github.io/Pagina_Catra/admin/Qr_generator.html
```

### Pasos para Generar un QR:

1. **Abre el generador de QR** usando la URL de arriba
2. **Ingresa el folio** de la constancia (debe existir en Google Sheets)
3. **Haz clic en "Generar Código QR"** o presiona Enter
4. **Descarga la imagen** del QR haciendo clic en "Descargar QR como PNG"
5. **Imprime o inserta** el QR en la constancia física

### Ventajas:
- ✅ Puedes usar el generador desde cualquier computadora con internet
- ✅ No necesitas instalar ningún programa
- ✅ Los QR generados son permanentes y funcionarán siempre
- ✅ Cualquier persona puede escanear el QR para verificar la autenticidad

---

## 📞 Soporte

Si tienes problemas o dudas, contacta al desarrollador del sistema.

**Fecha de última actualización:** Octubre 2025
