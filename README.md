# Central de Alarmas - Bomberos Teno

Pizarra digital interactiva para la central de alarmas del Cuerpo de Bomberos de Teno.

## 🚀 Inicio Rápido

1. Abre el archivo `index.html` directamente en tu navegador (doble clic)
2. La pizarra carga con datos de ejemplo
3. Haz clic en el botón ⚙️ (esquina inferior derecha) para acceder al panel de administración
4. Contraseña por defecto: `1234`

## 📋 Características

### Información en Pantalla
- ⏰ **Reloj y fecha** en tiempo real
- 📢 **Novedades** - lista de eventos y anuncios
- 📝 **Notas** - recordatorios y observaciones importantes
- 👨‍🚒 **Comandante de turno** - nombre y grado
- 🚒 **Unidad de turno** - identificación destacada
- 🟢 **Estado de unidades** - visualización con colores según estado
- 📞 **Contactos de emergencia** - números importantes
- 🏢 **Estado del cuartel** - OK / Alerta / Emergencia
- 🚨 **Maquinistas** - información de operadores

### Panel de Administración
- ✏️ Editar todo el contenido de la pizarra
- ➕ Agregar/eliminar unidades, novedades y contactos
- 📥 **Exportar configuración** a archivo JSON
- 📤 **Importar configuración** desde archivo JSON
- 🔒 Protección con contraseña

## 💾 Almacenamiento de Datos

La pizarra utiliza **dos sistemas de almacenamiento**:

### 1. LocalStorage (Automático)
Los cambios se guardan automáticamente en el navegador. Los datos persisten aunque cierres y vuelvas a abrir la página.

⚠️ **Importante**: Los datos en localStorage son específicos del navegador y dispositivo actual.

### 2. Archivos JSON (Manual)

#### Exportar Configuración
1. Abre el panel de administración (⚙️)
2. Ve a la sección **"Exportar / Importar configuración"**
3. Haz clic en **"📥 Exportar JSON"**
4. Se descargará el archivo `pizarra_config.json`

**Usos del archivo exportado:**
- ✅ Respaldo de seguridad
- ✅ Transferir configuración a otro dispositivo
- ✅ Edición manual con cualquier editor de texto
- ✅ Control de versiones (Git, etc.)

#### Importar Configuración
1. Abre el panel de administración (⚙️)
2. Ve a la sección **"Exportar / Importar configuración"**
3. Haz clic en **"📤 Importar JSON"**
4. Selecciona el archivo `.json` con la configuración
5. La pizarra se actualizará inmediatamente

#### Editar JSON Manualmente
Puedes editar el archivo JSON descargado con cualquier editor de texto. Ver `ejemplo_config.json` para el formato completo.

**Estructura básica:**
```json
{
  "novedades": ["Novedad 1", "Novedad 2"],
  "notas": "Texto de las notas",
  "comandante": {
    "name": "Nombre completo",
    "rank": "Grado"
  },
  "unidad": "B-1",
  "maquinistas": "Información de operadores",
  "cuartelNombre": "Cuartel 0-8",
  "cuartelEstado": "Operativo",
  "units": [
    { "name": "B-1", "status": "En servicio" }
  ],
  "contactos": [
    { "icon": "📞", "label": "Nombre", "value": "Número" }
  ],
  "password": "1234"
}
```

**Estados válidos para unidades:**
- `En servicio`
- `En espera`
- `Activo`
- `En mantención`
- `Fuera de servicio`

**Estados válidos para cuartel:**
- `Operativo` (verde)
- `Alarma` (amarillo)
- `FueraDeServicio` (rojo)

## 🔐 Cambiar Contraseña

1. Accede al panel de administración
2. Ve a la sección **"Cambiar contraseña"**
3. Ingresa la nueva contraseña
4. Haz clic en **"Guardar cambios"**

⚠️ **No olvides tu contraseña**: Si exportas la configuración, la contraseña también se exporta en el JSON (puedes recuperarla de ahí).

## 🖥️ Requisitos Técnicos

- Navegador moderno (Chrome, Firefox, Edge, Safari)
- No requiere conexión a internet
- No requiere instalación de software adicional
- No requiere servidor web

## 📱 Responsive

La pizarra se adapta automáticamente a diferentes tamaños de pantalla, ideal para:
- Monitores de TV
- Pantallas táctiles
- Tablets
- Computadoras de escritorio

## 🎨 Personalización

El diseño usa CSS variables para colores. Puedes modificar el tema editando las variables en el archivo HTML:

```css
:root {
  --bg:        #0d1b2a;  /* Fondo principal */
  --surface:   #162032;  /* Fondo de tarjetas */
  --border:    #1e3a5f;  /* Bordes */
  --accent:    #2563eb;  /* Color de acento */
  --gold:      #f59e0b;  /* Dorado para títulos */
  --green:     #22c55e;  /* Verde (activo) */
  --yellow:    #eab308;  /* Amarillo (alerta) */
  --red:       #ef4444;  /* Rojo (emergencia) */
}
```

## 📄 Archivos del Proyecto

- `index.html` - Archivo principal (contiene HTML, CSS y JavaScript)
- `ejemplo_config.json` - Ejemplo de archivo de configuración
- `README.md` - Esta documentación

## 🤝 Soporte

Para cualquier problema o sugerencia, contacta al administrador del sistema.