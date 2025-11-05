# Manual de Usuario - Virtual Card Gonzalo Frías

## 📋 Índice
1. [Introducción](#introducción)
2. [Navegación de la Página](#navegación-de-la-página)
3. [Solicitudes Disponibles](#solicitudes-disponibles)
4. [Arquitectura Web](#arquitectura-web)
5. [Guía de Desarrollo](#guía-de-desarrollo)
6. [Mantenimiento](#mantenimiento)

---

## 1. Introducción

Esta virtual card es una página web estática que funciona como tarjeta de presentación digital para Gonzalo Emilio Frías Ojeda, guía general en Torres del Paine. La página integra servicios propios de guiado con servicios asociados de comercios locales en Puerto Natales.

### Propósito
- Presentar información de contacto profesional
- Mostrar servicios de guiado disponibles
- Facilitar reservas y pagos
- Conectar con servicios asociados de la región

---

## 2. Navegación de la Página

### 2.1 Estructura de la Página

La página está organizada en **6 secciones principales**:

#### **A. Sección de Perfil**
- **Ubicación**: Parte superior
- **Contenido**: 
  - Foto de perfil profesional
  - Nombre completo
  - Rol: "Guía General en Torres del Paine"
  - Slogan: "Explora la Patagonia con un experto local"

#### **B. Sección de Contacto**
- **Botones disponibles**:
  - 🟢 **WhatsApp**: Contacto directo (+56 9 6132 4561)
  - 🔴 **Enviar correo**: friasgonzalo21@gmail.com
  - 🔴 **Enviar correo (2)**: economiegonzal@gmail.com
  - 🔵 **Perfil de LinkedIn**: Networking profesional
  - 🔵 **Ver Presentación IGP**: Presentación institucional en Prezi

#### **C. Servicios Destacados**
Lista de 9 servicios principales:
1. Trekking Base Torres
2. Circuito W
3. City Tours - Museos - Faro
4. Trekking Cerro Benítez
5. Circuito Cuevas
6. Mirador Cerro Dorotea
7. Tours de fotografía y avistamiento de fauna
8. Briefing Patagónico
9. Experiencias personalizadas

#### **D. Pagos y Reservas**
- Código QR para pagos digitales
- Botón de calendario de Google para verificar disponibilidad
- Enlace directo a agenda pública

#### **E. Servicios Asociados** *(Nueva funcionalidad)*
Cuatro categorías de servicios lateralizados:

**🍽️ Alimentación**
- Supermercado Local: Provisiones para trekking y tours
- Restaurantes Asociados: Comida típica patagónica
- Panadería y Café: Desayunos y snacks para viaje

**🏥 Salud y Bienestar**
- Farmacia Local: Medicamentos y primeros auxilios
- Centro Médico: Atención médica turística
- Fisioterapia Deportiva: Recuperación post-trekking

**🚌 Transporte**
- Transfer Aeropuerto: Punta Arenas - Puerto Natales
- Buses al Parque: Traslados a Torres del Paine
- Rent a Car: Alquiler de vehículos 4x4

**🛒 E-Commerce y Reventa**
- Equipamiento Outdoor: Venta y alquiler de equipo
- Souvenirs Locales: Artesanías patagónicas
- Paquetes Combinados: Tours + servicios complementarios

---

## 3. Solicitudes Disponibles

### 3.1 Para Clientes/Turistas

#### **Solicitar Información de Tours**
1. Hacer clic en el botón verde **WhatsApp**
2. Se abre conversación con mensaje pre-cargado
3. Consultar sobre servicios específicos

#### **Reservar un Tour**
1. Revisar servicios en la sección "Servicios Destacados"
2. Verificar disponibilidad usando el botón **"Ver mi disponibilidad"**
3. Contactar vía WhatsApp o email para confirmar
4. Realizar pago escaneando el código QR

#### **Consultar Servicios Asociados**
1. Navegar a la sección "Servicios Asociados"
2. Revisar las 4 categorías disponibles
3. Hacer clic en **"Consultar Servicios Asociados"** (botón verde al final)
4. Se abre WhatsApp con mensaje específico pre-cargado:
   - "Hola, me interesa información sobre servicios asociados"

### 3.2 Para Comercios Asociados

#### **Solicitar Ser Partner**
1. Contactar vía email: friasgonzalo21@gmail.com o economiegonzal@gmail.com
2. Asunto: "Solicitud Partnership - [Nombre Comercio]"
3. Incluir:
   - Nombre del comercio
   - Categoría de servicio (Alimentación, Salud, Transporte, E-commerce)
   - Descripción breve del servicio
   - Información de contacto

#### **Actualizar Información de Partner**
- Contactar al administrador vía email
- Proporcionar datos actualizados

---

## 4. Arquitectura Web

### 4.1 Estructura de Archivos

```
vcard/
├── index.html              # Página principal (estructura HTML)
├── style.css               # Estilos visuales (diseño y layout)
├── vcard_stats.html        # Página de estadísticas (opcional)
├── documents/              # Recursos multimedia
│   ├── guidepic.jpg        # Foto de perfil
│   ├── cert_sernatur.pdf   # Certificación SERNATUR
│   ├── cert_liderazgo_uandes.pdf
│   ├── WFR Gonzalo.pdf     # Certificado Wilderness First Responder
│   ├── credencial-gf-ggral.jpg
│   └── turismo - Sheet1.csv
└── qr-pagos.png           # Código QR para pagos (si existe)
```

### 4.2 Tecnologías Utilizadas

#### **Frontend**
- **HTML5**: Estructura semántica
- **CSS3**: Diseño responsive y estilos
- **Font Awesome 6.5.1**: Iconografía (CDN)
- **Chart.js**: Gráficos estadísticos (en vcard_stats.html)

#### **Dependencias Externas**
```html
<!-- Font Awesome Icons -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

<!-- Chart.js (solo en vcard_stats.html) -->
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
```

### 4.3 Diseño Responsive

El sitio está optimizado para:
- 📱 **Móviles**: 320px - 767px
- 💻 **Tablets**: 768px - 1024px
- 🖥️ **Desktop**: 1025px+

**Características responsive**:
- Layout adaptable con flexbox
- Tarjeta con ancho máximo de 450px
- Botones de contacto en bloque al 100% de ancho
- Imágenes escalables

### 4.4 Paleta de Colores

```css
/* Colores principales */
Azul primario:    #007bff  /* Títulos y acentos */
Verde WhatsApp:   #25d366  /* Botón WhatsApp */
Rojo email:       #dc3545  /* Botones email */
Azul LinkedIn:    #0077b5  /* LinkedIn */
Amarillo reservas: #ffc107  /* Calendario */

/* Colores de fondo */
Fondo página:     #e9ecef  /* Gris claro */
Fondo tarjeta:    #ffffff  /* Blanco */
Fondo items:      #f8f9fa  /* Gris muy claro */

/* Textos */
Principal:        #343a40  /* Negro suave */
Secundario:       #6c757d  /* Gris medio */
Terciario:        #495057  /* Gris oscuro */
```

---

## 5. Guía de Desarrollo

### 5.1 Requisitos Previos

- Editor de código (VS Code, Sublime Text, etc.)
- Navegador web moderno (Chrome, Firefox, Edge)
- Git (para control de versiones)
- Conocimientos básicos de HTML/CSS

### 5.2 Configuración del Entorno Local

#### **Paso 1: Clonar el Repositorio**
```bash
git clone https://github.com/gonzal-21/vcard.git
cd vcard
```

#### **Paso 2: Abrir con Servidor Local**

**Opción A - Python**:
```bash
python3 -m http.server 8080
# Abrir: http://localhost:8080
```

**Opción B - Node.js (http-server)**:
```bash
npm install -g http-server
http-server -p 8080
# Abrir: http://localhost:8080
```

**Opción C - VS Code Live Server**:
1. Instalar extensión "Live Server"
2. Click derecho en `index.html` → "Open with Live Server"

### 5.3 Modificaciones Comunes

#### **Actualizar Información de Contacto**

**Archivo**: `index.html`

```html
<!-- Cambiar número de WhatsApp -->
<a href="https://wa.me/56961324561" target="_blank" class="link-btn whatsapp-btn">

<!-- Cambiar emails -->
<a href="mailto:friasgonzalo21@gmail.com" class="link-btn email-btn">
<a href="mailto:economiegonzal@gmail.com" class="link-btn email-btn">

<!-- Cambiar LinkedIn -->
<a href="https://www.linkedin.com/in/gonzalof21/" target="_blank" class="link-btn linkedin-btn">
```

#### **Agregar Nuevo Servicio**

**Archivo**: `index.html` (línea ~40-52)

```html
<div class="services-section">
  <h2><i class="fas fa-mountain"></i> Servicios Destacados</h2>
  <ul>
    <!-- Servicios existentes -->
    <li id="service10">Nuevo Servicio Aquí</li>  <!-- AGREGAR -->
  </ul>
</div>
```

#### **Modificar Servicios Asociados**

**Archivo**: `index.html` (línea ~72-150)

```html
<!-- Ejemplo: Agregar nuevo partner en categoría Alimentación -->
<div class="partner-category">
  <h3><i class="fas fa-utensils"></i> Alimentación</h3>
  <ul class="partner-list">
    <!-- Partners existentes -->
    <li>
      <span class="partner-name">Nuevo Partner</span>
      <span class="partner-desc">Descripción del servicio</span>
    </li>
  </ul>
</div>
```

#### **Cambiar Colores del Tema**

**Archivo**: `style.css`

```css
/* Modificar color principal */
h1 {
    color: #007bff;  /* Cambiar por color deseado */
}

/* Modificar botón WhatsApp */
.whatsapp-btn { 
    background-color: #25d366;  /* Cambiar color */
}
```

#### **Actualizar Foto de Perfil**

1. Reemplazar archivo: `documents/guidepic.jpg`
2. Mantener nombre o actualizar referencia en HTML:
```html
<img src="/documents/guidepic.jpg" alt="Guía en Parque Nacional Torres del Paine" class="profile-pic">
```

### 5.4 Agregar Nueva Categoría de Servicios Asociados

**Paso 1**: Editar `index.html`
```html
<div class="partner-category">
  <h3><i class="fas fa-NEW-ICON"></i> Nueva Categoría</h3>
  <ul class="partner-list">
    <li>
      <span class="partner-name">Nombre del Partner</span>
      <span class="partner-desc">Descripción breve</span>
    </li>
  </ul>
</div>
```

**Paso 2**: Iconos disponibles en Font Awesome:
- 🍽️ `fa-utensils` - Alimentación
- 🏥 `fa-medkit` - Salud
- 🚌 `fa-bus` - Transporte
- 🛒 `fa-shopping-cart` - E-commerce
- 🏠 `fa-home` - Alojamiento
- 🎨 `fa-palette` - Arte/Cultura
- 📷 `fa-camera` - Fotografía

Ver más en: https://fontawesome.com/icons

### 5.5 Testing y Validación

#### **Validar HTML**
```bash
# Usando validador online
# https://validator.w3.org/

# O con Python:
python3 -c "
from html.parser import HTMLParser
with open('index.html', 'r') as f:
    HTMLParser().feed(f.read())
print('HTML válido')
"
```

#### **Validar CSS**
- Usar: https://jigsaw.w3.org/css-validator/

#### **Test Responsive**
1. Abrir Chrome DevTools (F12)
2. Activar "Toggle device toolbar" (Ctrl+Shift+M)
3. Probar en:
   - iPhone SE (375px)
   - iPhone 12 Pro (390px)
   - iPad (768px)
   - Desktop (1920px)

#### **Test de Navegadores**
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+

---

## 6. Mantenimiento

### 6.1 Actualización de Contenido

#### **Frecuencia Recomendada**
- 📅 **Mensual**: Revisar disponibilidad de calendario
- 🏢 **Trimestral**: Actualizar servicios asociados
- 📊 **Semestral**: Actualizar estadísticas (vcard_stats.html)
- 📄 **Anual**: Renovar certificaciones en carpeta documents

#### **Checklist de Actualización**
```markdown
- [ ] Verificar enlaces externos funcionan
- [ ] Comprobar número de WhatsApp activo
- [ ] Revisar emails de contacto
- [ ] Actualizar servicios asociados
- [ ] Verificar código QR de pagos
- [ ] Comprobar enlace de calendario Google
- [ ] Revisar presentación Prezi actualizada
- [ ] Validar certificados PDF accesibles
```

### 6.2 Gestión de Partners

#### **Agregar Nuevo Partner**
1. Identificar categoría apropiada
2. Solicitar información al comercio:
   - Nombre comercial
   - Descripción breve (máx. 50 caracteres)
   - Contacto del responsable
3. Agregar en HTML siguiendo formato existente
4. Probar visualización responsive
5. Commitear cambios a Git

#### **Remover Partner**
1. Localizar entrada en HTML
2. Eliminar bloque `<li>...</li>` correspondiente
3. Verificar que quedan al menos 2 partners por categoría
4. Commitear cambios

### 6.3 Backup y Versionado

#### **Git Workflow**
```bash
# 1. Crear rama para cambios
git checkout -b feature/actualizar-partners

# 2. Hacer cambios en archivos
# Editar index.html, style.css, etc.

# 3. Revisar cambios
git status
git diff

# 4. Commitear
git add .
git commit -m "Actualizar partners en categoría Transporte"

# 5. Pushear a GitHub
git push origin feature/actualizar-partners

# 6. Crear Pull Request en GitHub
```

#### **Backup Recomendado**
- **Automático**: GitHub (repositorio remoto)
- **Local**: Copia semanal en disco externo
- **Cloud**: Google Drive / Dropbox (carpeta documents/)

### 6.4 Optimización

#### **Imágenes**
```bash
# Comprimir foto de perfil
# Usar: https://tinypng.com/
# Objetivo: < 200KB, 500x500px

# Optimizar QR
# Formato: PNG, 300x300px, < 50KB
```

#### **Performance**
- ✅ Página carga < 2 segundos
- ✅ Imágenes optimizadas
- ✅ CSS minificado (opcional para producción)
- ✅ Sin JavaScript innecesario

### 6.5 SEO Básico

**Agregar meta tags en `<head>`**:
```html
<meta name="description" content="Gonzalo Frías - Guía oficial Torres del Paine. Trekking Base Torres, Circuito W, tours personalizados en la Patagonia.">
<meta name="keywords" content="guia torres del paine, trekking patagonia, circuito w, puerto natales">
<meta name="author" content="Gonzalo Emilio Frías Ojeda">

<!-- Open Graph para redes sociales -->
<meta property="og:title" content="Gonzalo Frías - Guía Torres del Paine">
<meta property="og:description" content="Explora la Patagonia con un experto local">
<meta property="og:image" content="/documents/guidepic.jpg">
<meta property="og:url" content="https://gonzal-21.github.io/vcard/">
```

---

## 7. Solución de Problemas

### Problema: Enlaces de WhatsApp no funcionan
**Solución**: Verificar formato correcto:
```html
<a href="https://wa.me/56961324561?text=Mensaje" target="_blank">
```

### Problema: Código QR no se muestra
**Solución**: 
1. Verificar que existe `qr-pagos.png` en raíz
2. Comprobar permisos del archivo
3. Verificar ruta en HTML

### Problema: Estilos no se aplican
**Solución**:
1. Limpiar caché del navegador (Ctrl+F5)
2. Verificar ruta de `style.css` en HTML
3. Comprobar sintaxis CSS válida

### Problema: Página no responsive en móvil
**Solución**: Verificar meta viewport en HTML:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

---

## 8. Contacto y Soporte

### Para Desarrollo/Técnico
- **GitHub Issues**: https://github.com/gonzal-21/vcard/issues
- **Email técnico**: economiegonzal@gmail.com

### Para Servicios/Comercial
- **WhatsApp**: +56 9 6132 4561
- **Email**: friasgonzalo21@gmail.com

---

## 9. Recursos Adicionales

### Documentación
- **HTML5**: https://developer.mozilla.org/es/docs/Web/HTML
- **CSS3**: https://developer.mozilla.org/es/docs/Web/CSS
- **Font Awesome**: https://fontawesome.com/docs
- **Git**: https://git-scm.com/doc

### Herramientas Recomendadas
- **Editor**: Visual Studio Code (https://code.visualstudio.com/)
- **Control de versiones**: GitHub Desktop (https://desktop.github.com/)
- **Diseño**: Figma (https://www.figma.com/)
- **Optimización de imágenes**: TinyPNG (https://tinypng.com/)

---

## Anexo: Glosario

- **Virtual Card**: Tarjeta de presentación digital interactiva
- **Lateralización**: Colaboración con servicios complementarios de terceros
- **Responsive**: Diseño adaptable a diferentes tamaños de pantalla
- **CDN**: Content Delivery Network (red de distribución de contenido)
- **QR**: Quick Response (código de respuesta rápida)
- **CTA**: Call To Action (llamado a la acción)
- **SEO**: Search Engine Optimization (optimización para motores de búsqueda)

---

**Versión del Manual**: 1.0  
**Última actualización**: Noviembre 2025  
**Autor**: Copilot Agent  
**Licencia**: Uso interno
