# 🗳️ Células Ciudadanas

> **Sistema de gestión para la organización política ciudadana a nivel de barrio.**  
> Administra células, miembros, tareas, reportes y comunicación — todo desde un solo archivo HTML sin necesidad de servidor ni instalación.

---

## 📋 Descripción

**Células Ciudadanas** es una aplicación web completa y autónoma diseñada para coordinadores de movimientos ciudadanos que necesitan organizar grupos de base (células) a nivel de barrio o sector. Funciona como un archivo HTML independiente que se ejecuta directamente en cualquier navegador moderno.

Todos los datos se guardan automáticamente en el almacenamiento local del navegador (`localStorage`), con soporte completo para exportar backups, restaurar datos e imprimir informes profesionales.

---

## ✨ Características principales

### 📊 Dashboard general
- KPIs en tiempo real: células activas, miembros totales, hogares contactados, días para elecciones
- Semáforo de células (en meta / en riesgo / inactiva)
- Barras de progreso hacia metas
- Actividad reciente del sistema
- Tabla resumen por célula con enlace directo a WhatsApp

### 🏘️ Gestión de células
- Crear y administrar células por barrio o sector
- Visualización de miembros, hogares contactados y porcentaje de meta
- Estados: activa, en riesgo, nueva
- Enlace directo a WhatsApp del líder desde la tarjeta

### 👥 Directorio de miembros
- Registro completo: nombre, barrio, celular, célula asignada, rol
- Búsqueda en tiempo real por nombre o barrio
- Filtros por célula y por rol
- Enlace directo a WhatsApp de cada miembro
- Roles: Líder, Vocero, Secretario, Veedor, Miembro

### ✅ Tareas semanales
- Gestión de tareas por célula o para toda la red
- Marcado de completadas en tiempo real
- Prioridad: Alta, Media, Baja
- Barra de progreso semanal
- Filtro por célula mediante pestañas

### 📈 Reportes de avance
- Informe semanal automático con fecha
- Resumen de 6 métricas clave
- Tabla detallada por célula con WhatsApp
- Función para copiar reporte formateado para WhatsApp

### 💬 Mensajes para WhatsApp
- Banco de mensajes listos para copiar: lunes, miércoles, viernes, motivación y día de elecciones
- Botón de copia individual por mensaje
- Enlace directo al coordinador principal vía WhatsApp

### 💾 Backup y recuperación
- **Exportar**: Descarga un archivo `.json` con todos los datos (células, miembros, tareas, actividad)
- **Restaurar**: Importa un `.json` previamente exportado con backup automático previo
- **Imprimir todo**: Genera informe completo en A4 de todas las secciones
- **Borrar datos**: Limpia el localStorage con backup automático antes
- Historial de los últimos 12 backups con fecha y estadísticas
- Indicador de tamaño del almacenamiento local usado

### ⚙️ Configuración
- Fecha de elecciones con cuenta regresiva automática en el dashboard
- Número WhatsApp del coordinador (enlace directo desde Mensajes)

---

## 🚀 Instalación y uso

### Requisitos
- Cualquier navegador web moderno (Chrome, Firefox, Edge, Safari)
- **No requiere servidor**
- **No requiere instalación**
- **No requiere conexión a internet** (excepto para cargar fuentes de Google Fonts la primera vez)

### Pasos para usar

1. **Descarga** el archivo `app_celulas_VPH.html`
2. **Ábrelo** directamente en tu navegador (doble clic o arrastrar al navegador)
3. **Configura** tu número de WhatsApp y la fecha de elecciones en la sección **Backup → Configuración**
4. **Comienza** a registrar células y miembros

```
No necesitas instalar nada. Solo abre el archivo HTML en tu navegador.
```

---

## 💾 Persistencia de datos

Los datos se guardan automáticamente en el `localStorage` del navegador:

- **Guardado automático** cada 30 segundos
- **Guardado inmediato** al crear o modificar cualquier dato
- **Indicador visual** en el sidebar que confirma cada guardado
- Los datos **persisten** al cerrar y reabrir el navegador
- Los datos son **locales al navegador y dispositivo** — no se envían a ningún servidor

> ⚠️ **Importante**: Si limpias el caché del navegador o usas modo incógnito, los datos se perderán. Exporta un backup regularmente.

---

## 📤 Sistema de Backup

### Exportar backup
1. Ve a la sección **Backup** en el menú lateral
2. Haz clic en **⬇ Descargar .json**
3. Se descarga un archivo con nombre: `backup_celulas_YYYY-MM-DD_HH-MM.json`

### Restaurar backup
1. Ve a la sección **Backup**
2. Haz clic en **⬆ Seleccionar .json**
3. Selecciona el archivo de backup previamente exportado
4. Confirma la restauración — se hará un backup automático antes de reemplazar los datos

### Backup automático
El sistema genera un backup automático antes de:
- Restaurar datos desde un archivo
- Borrar todos los datos

---

## 🖨️ Impresión de informes

Cada sección tiene su propio botón **🖨 Imprimir** que genera una versión limpia en A4 con:
- Encabezado con nombre de la app y fecha de generación
- Diseño optimizado para impresión (fondo blanco, texto negro)
- Sin sidebar ni botones de acción

Para imprimir **todas las secciones** de una vez:
1. Ve a **Backup**
2. Haz clic en **🖨 Imprimir todo**

---

## 📱 Integración con WhatsApp

Cada número telefónico registrado (líderes y miembros) genera automáticamente un enlace directo a WhatsApp:

- **Formato aceptado**: 10 dígitos (ej: `3117700431`) — el sistema agrega automáticamente el código de Colombia `57`
- **También acepta**: formato completo `573117700431`
- Los enlaces aparecen en: tarjetas de células, directorio de miembros, tabla de reportes y resumen del dashboard
- El número del coordinador principal aparece como botón de contacto en la sección **Mensajes**

---

## 🗂️ Estructura del proyecto

```
app_celulas_VPH.html     ← Archivo único con toda la aplicación
README.md                ← Este archivo
```

La aplicación es un **single-file app**: todo el HTML, CSS y JavaScript está contenido en un único archivo de ~1,100 líneas, sin dependencias externas excepto las fuentes de Google Fonts.

---

## 🧩 Módulos de la aplicación

| Módulo | Descripción |
|--------|-------------|
| Dashboard | Resumen general con KPIs y semáforo |
| Células | Gestión de grupos por barrio/sector |
| Miembros | Directorio con búsqueda y filtros |
| Tareas | Seguimiento semanal de compromisos |
| Reportes | Informe semanal con función de copia |
| Mensajes | Banco de mensajes para WhatsApp |
| Backup | Exportar, restaurar, imprimir y configurar |

---

## 🔧 Tecnologías utilizadas

| Tecnología | Uso |
|------------|-----|
| HTML5 | Estructura y markup |
| CSS3 | Estilos, animaciones y diseño responsivo |
| JavaScript (ES6+) | Lógica de la aplicación |
| localStorage API | Persistencia de datos local |
| Clipboard API | Copia de mensajes |
| File API | Importación de backups |
| Google Fonts (Syne + DM Sans) | Tipografía |

---

## 📐 Diseño

- **Tema**: Oscuro (dark mode nativo)
- **Tipografía**: Syne (títulos) + DM Sans (cuerpo)
- **Paleta principal**: Púrpura `#4A3FD4`, Verde `#0C8A60`, Coral `#C93B1C`, Ámbar `#B8680A`
- **Responsivo**: Adaptado para móvil (sidebar oculto en pantallas pequeñas)
- **Impresión**: Estilos dedicados `@media print` con diseño limpio en blanco

---

## 📊 Datos de muestra (demo)

La aplicación incluye datos de demostración al abrirse por primera vez:

- **6 células** en Caucasia, Antioquia
- **10 miembros** con roles asignados
- **8 tareas** semanales (algunas completadas)
- **5 registros** de actividad reciente

Estos datos se reemplazan automáticamente al registrar información real.

---

## 🔒 Privacidad y seguridad

- **Sin servidor**: Todos los datos permanecen en el dispositivo del usuario
- **Sin cookies**: No se usa ningún sistema de rastreo
- **Sin APIs externas**: No se envía información a terceros
- **Código abierto**: Todo el código es visible e inspeccionable en el archivo HTML
- Los números de WhatsApp generan enlaces directos a `wa.me` — WhatsApp no requiere que el número esté en la agenda

---

## 🌐 Compatibilidad de navegadores

| Navegador | Soporte |
|-----------|---------|
| Chrome 80+ | ✅ Completo |
| Firefox 75+ | ✅ Completo |
| Edge 80+ | ✅ Completo |
| Safari 13+ | ✅ Completo |
| Opera 67+ | ✅ Completo |
| IE 11 | ❌ No soportado |

---

## 📝 Guía rápida de inicio

### 1. Configurar el sistema
```
Backup → Configuración
→ Ingresar fecha de elecciones
→ Ingresar número WhatsApp del coordinador (ej: 573117700431)
```

### 2. Crear la primera célula
```
Células → + Nueva célula
→ Nombre del barrio
→ Nombre y celular del líder
→ Crear célula
```

### 3. Registrar miembros
```
Miembros → + Nuevo miembro
→ Nombre, barrio, celular
→ Asignar a una célula
→ Asignar rol
→ Registrar
```

### 4. Asignar tareas semanales
```
Tareas → + Nueva tarea
→ Descripción de la tarea
→ Asignar célula (o todas)
→ Prioridad
→ Agregar tarea
```

### 5. Exportar backup semanal
```
Backup → ⬇ Descargar .json
→ Guardar en carpeta segura o Google Drive
```

---

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Por favor:

1. Haz un fork del repositorio
2. Crea una rama con tu feature: `git checkout -b feature/nueva-funcionalidad`
3. Haz commit de tus cambios: `git commit -m 'Agrega nueva funcionalidad'`
4. Push a la rama: `git push origin feature/nueva-funcionalidad`
5. Abre un Pull Request

---

## 📄 Licencia

Este proyecto está bajo licencia propietaria.

**© Vibras Positivas HM — Todos los Derechos Reservados**

Queda prohibida la reproducción, distribución o modificación de este software sin autorización expresa del autor.

---

## 👨‍💻 Desarrollador

**Vibras Positivas HM**  
📱 WhatsApp: [+57 311 770 0431](https://wa.me/573117700431)

---

<div align="center">

**Desarrollada por Vibras Positivas HM — Derechos de Autor Reservados**

</div>
