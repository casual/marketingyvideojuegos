# Plan de Creación: Blog "Marketing y Videojuegos"

## Objetivo
Crear un blog sencillo usando Jekyll con el tema jekyll-garden que:
- Reciba contenido desde archivos Markdown de Obsidian
- Sea fácil de mantener y actualizar
- Tenga bajo consumo de recursos
- Permita agregar y editar artículos de forma sencilla

## Tema Base
**Jekyll Garden**: https://github.com/Jekyll-Garden/jekyll-garden.github.io
- Diseñado específicamente para integración con Obsidian
- Soporta enlaces tipo wiki `[[nota]]`
- Vista previa de enlaces al pasar el cursor
- Backlinks automáticos
- Modo oscuro/claro incluido

## Fase 1: Configuración Inicial del Proyecto

### 1.1 Requisitos Previos
Instalar en tu sistema:
- **Ruby** (versión 2.7 o superior)
- **Bundler** (gestor de gemas de Ruby)
- **Git** (para control de versiones)
- **Obsidian** (ya lo tienes)

Alternativa simplificada con Docker:
- Solo necesitas Docker Desktop instalado
- Evita configurar Ruby y dependencias manualmente

### 1.2 Descarga e Instalación
```bash
# Clonar el tema jekyll-garden como base
git clone https://github.com/Jekyll-Garden/jekyll-garden.github.io marketingyvideojuegos
cd marketingyvideojuegos

# Instalar dependencias
bundle install

# Probar localmente
bundle exec jekyll serve
```

El sitio estará disponible en `http://localhost:4000`

### 1.3 Configuración Básica (_config.yml)
Editar el archivo `_config.yml` con:
```yaml
title: "Marketing y Videojuegos"
heading: "[Tu nombre o nombre del autor]"
description: "Análisis y estrategias de marketing en la industria de videojuegos"
url: "[URL de tu sitio]"
baseurl: "" # Dejar vacío si usas dominio propio o subdomain.github.io
```

## Fase 2: Estructura de Contenido

### 2.1 Organización de Carpetas
```
marketingyvideojuegos/
├── _notes/              # Aquí van tus artículos de Obsidian
│   ├── marketing/       # (opcional) subcarpetas por tema
│   ├── videojuegos/
│   └── analisis/
├── _includes/           # Componentes reutilizables
├── _layouts/            # Plantillas de diseño
├── assets/              # CSS, JS, imágenes
│   ├── css/
│   ├── js/
│   └── img/
├── _config.yml          # Configuración principal
└── Gemfile              # Dependencias Ruby
```

### 2.2 Formato de Artículos
Cada artículo en `_notes/` debe tener este formato:

```markdown
---
title: "Título del Artículo"
date: 2025-11-29
tags: [marketing, videojuegos, estrategia]
---

# Contenido del artículo

Tu contenido aquí. Puedes usar enlaces tipo Obsidian [[otro-articulo]]
```

## Fase 3: Flujo de Trabajo con Obsidian

### 3.1 Opciones de Integración
[PENDIENTE: Definir según preferencias del usuario]

**Opción A - Copia Manual**
- Bóveda Obsidian separada
- Copias archivos manualmente a `_notes/`
- Mayor control sobre qué se publica

**Opción B - Carpeta Compartida**
- `_notes/` es parte de tu bóveda Obsidian
- Cambios automáticos reflejados
- Más rápido para publicar

**Opción C - Sincronización Automatizada**
- Script que copia archivos marcados
- Uso de plugin de Obsidian
- Balance entre control y automatización

### 3.2 Agregar Nuevo Artículo
1. Crear archivo `.md` en `_notes/`
2. Agregar front matter (título, fecha, tags)
3. Escribir contenido en Markdown
4. Guardar archivo
5. Jekyll regenera automáticamente el sitio

### 3.3 Editar Artículo Existente
1. Abrir archivo en `_notes/`
2. Hacer cambios
3. Guardar
4. Jekyll actualiza automáticamente

## Fase 4: Personalización Visual

### 4.1 Personalización Básica
Editar `_config.yml` para:
- Título y descripción del sitio
- Información del autor
- Enlaces de redes sociales
- Favicon

### 4.2 Estilos CSS
Modificar `assets/css/style.css` para:
- Colores del tema
- Tipografía
- Espaciados y márgenes
- Diseño responsive

### 4.3 Componentes Personalizables
- `_includes/header.html` - Cabecera del sitio
- `_includes/footer.html` - Pie de página
- `_layouts/default.html` - Plantilla base
- `_layouts/post.html` - Plantilla de artículos

## Fase 5: Despliegue y Publicación

### 5.1 Opciones de Hosting
[PENDIENTE: Definir según preferencias del usuario]

**GitHub Pages (Recomendado para simplicidad)**
- Gratis
- Integración automática con Git
- URL: `tuusuario.github.io/marketingyvideojuegos`
- Actualización automática al hacer push

**Netlify (Más características)**
- Gratis para proyectos pequeños
- Dominio personalizado fácil
- Formularios y funciones serverless
- Pre-visualización de cambios

### 5.2 Proceso de Publicación
```bash
# Agregar cambios
git add .

# Crear commit
git commit -m "Nuevo artículo: [título]"

# Publicar
git push origin main
```

## Fase 6: Mantenimiento Continuo

### 6.1 Flujo de Trabajo Regular
1. Escribir artículo en Obsidian
2. Mover/copiar a `_notes/`
3. Probar localmente: `bundle exec jekyll serve`
4. Revisar en `localhost:4000`
5. Publicar: `git push`

### 6.2 Actualizaciones del Tema
```bash
# Verificar actualizaciones de gemas
bundle update

# Actualizar tema (si hay cambios upstream)
git remote add upstream https://github.com/Jekyll-Garden/jekyll-garden.github.io
git fetch upstream
git merge upstream/main
```

### 6.3 Backup
- El repositorio Git es tu backup principal
- Considerar copias locales de `_notes/`
- Exportar configuración `_config.yml`

## Recursos de Consumo

### Ventajas de Bajo Consumo
- Sitio estático (solo HTML/CSS/JS)
- No requiere base de datos
- No requiere servidor dinámico
- Hosting gratuito en GitHub Pages/Netlify
- Builds rápidos (segundos)

### Requisitos Técnicos Mínimos
- **Desarrollo local**: 2GB RAM, Ruby instalado
- **Hosting**: 0€/mes con GitHub Pages o Netlify
- **Almacenamiento**: ~50MB para sitio básico
- **Build time**: 5-10 segundos por cambio

## Próximos Pasos

### Decisiones Pendientes
1. ¿Dónde hospedar el blog? (GitHub Pages / Netlify / Otro)
2. ¿Cómo integrar con Obsidian? (Manual / Carpeta compartida / Automatizado)
3. ¿Nivel de personalización visual inicial?
4. ¿Organización de contenido? (Tags / Carpetas / Ambos)
5. ¿Usar Ruby directamente o Docker?

### Orden de Ejecución
Una vez respondidas las preguntas:
1. Configurar entorno de desarrollo
2. Clonar y configurar tema base
3. Personalizar configuración y estilos
4. Crear estructura de contenido
5. Importar/crear primeros artículos de prueba
6. Configurar hosting y despliegue
7. Publicar primera versión
8. Documentar flujo de trabajo para uso continuo

## Guía Rápida de Comandos

```bash
# Desarrollo local
bundle exec jekyll serve          # Iniciar servidor local
bundle exec jekyll serve --drafts # Incluir borradores

# Limpiar archivos generados
bundle exec jekyll clean

# Build para producción
JEKYLL_ENV=production bundle exec jekyll build

# Git
git status                        # Ver cambios
git add .                         # Agregar todos los cambios
git commit -m "mensaje"           # Crear commit
git push                          # Publicar cambios
```

## Documentación de Referencia
- [Jekyll Garden Repository](https://github.com/Jekyll-Garden/jekyll-garden.github.io)
- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [Markdown Guide](https://www.markdownguide.org/)
- [Obsidian Help](https://help.obsidian.md/)

---

**Nota**: Este plan se irá refinando según tus respuestas a las preguntas de clarificación.