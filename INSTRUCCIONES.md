# Instrucciones de Compilación - Marketing y Videojuegos

## Resumen del Proyecto

Este es un sitio estático generado con **Jekyll 4.3.0** usando el tema **Minimal Mistakes**. El proyecto convierte archivos Markdown (notas) en páginas HTML estáticas.

---

## Cómo Compilar el Sitio

### Opción 1: Compilación Local (Recomendado)

**Requisitos previos:**
- Ruby 3.4.0+ instalado
- Bundler instalado (`gem install bundler`)

**Comandos:**

```bash
# 1. Instalar dependencias (primera vez o después de cambios en Gemfile)
bundle install

# 2. Compilar y servir el sitio localmente
bundle exec jekyll serve

# El sitio estará disponible en http://localhost:4000
# Los cambios se recompilan automáticamente
```

**Solo compilar sin servidor local:**

```bash
bundle exec jekyll build
```

Esto genera el sitio estático en la carpeta `_site/`

---

### Opción 2: Compilación con Docker

**Requisitos previos:**
- Docker y Docker Compose instalados

**Comandos:**

```bash
# Levantar el contenedor y servir el sitio
docker-compose up

# El sitio estará disponible en http://localhost:4000
```

---

### Opción 3: Compilación de Producción (Netlify)

El sitio se despliega automáticamente en Netlify cuando haces push a tu repositorio. El comando usado es:

```bash
bundle config set force_ruby_platform true && bundle install && bundle exec jekyll build
```

---

## Estructura de Directorios

### Contenido Fuente (Notas que se convierten en páginas):

- **`_casos-de-exito/`** - Casos de éxito de marketing de videojuegos
- **`_industria/`** - Análisis de la industria
- **`_tips-y-estrategias/`** - Consejos y estrategias de marketing
- **`_pages/`** - Páginas estáticas (about, archivos, etc.)
- **`index.md`** - Página de inicio

### Salida:

- **`_site/`** - Sitio HTML generado (no incluir en git)

---

## Proceso de Conversión

1. Jekyll lee los archivos `.md` de las carpetas de contenido
2. Procesa el YAML frontmatter (título, fecha, categorías, tags)
3. Convierte Markdown a HTML usando Kramdown
4. Aplica el layout del tema Minimal Mistakes
5. Genera páginas HTML estáticas en `_site/`
6. Crea feeds RSS, sitemap XML, y páginas de archivo automáticamente

---

## Archivos de Configuración Clave

- **`_config.yml`** - Configuración principal de Jekyll
- **`Gemfile`** - Dependencias Ruby
- **`netlify.toml`** - Configuración de deployment
- **`_data/navigation.yml`** - Menú de navegación
- **`_data/authors.yml`** - Perfiles de autores

---

## Comandos Útiles

```bash
# Ver versión de Jekyll
bundle exec jekyll --version

# Limpiar el sitio generado
bundle exec jekyll clean

# Compilar con modo de producción
JEKYLL_ENV=production bundle exec jekyll build

# Ver configuración actual
bundle exec jekyll doctor
```

---

## Solución de Problemas

Si encuentras errores:

### 1. Dependencias desactualizadas:
```bash
bundle update
```

### 2. Cache corrupto:
```bash
bundle exec jekyll clean
rm -rf _site .jekyll-cache
bundle exec jekyll serve
```

### 3. Problemas de versión de Ruby:
Verifica que estés usando Ruby 3.4.0+ con:
```bash
ruby -v
```

---

## Resultado

Después de compilar:
- Las notas Markdown se convierten en páginas HTML individuales
- Se generan índices por categorías y tags
- Se crea un feed RSS automáticamente
- Se genera un sitemap.xml para SEO
- Todo el sitio estático queda en la carpeta `_site/`
