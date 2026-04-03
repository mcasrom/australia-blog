---
title: "Cómo Escribir Nuevos Posts en Hugo (Guía Operativa)"
date: 2026-04-03T16:40:00+02:00
draft: false
tags: ["hugo", "blog", "linux", "workflow"]
showToc: true
---

## Introducción

Durante el mantenimiento del blog en el ODROID C2 con DietPi es habitual confundirse entre las carpetas **content/** y **docs/**.  
Este post aclara de forma directa dónde deben escribirse los artículos y cómo integrarlos en el flujo de trabajo del proyecto *travel‑station*.

---

## Dónde se Escriben Realmente los Posts

Hugo utiliza dos rutas distintas:

### 📌 1. Carpeta **content/** → Aquí se escriben los posts
Ruta real:


Todo lo que escribas aquí debe ser un archivo `.md` con front matter.

Ejemplo:


### 🚫 2. Carpeta **docs/** → Salida generada (NO editar)
Ruta:



Esta carpeta contiene solo HTML generado por Hugo.  
Cada vez que ejecutas `hugo` o tu script de despliegue, **se sobrescribe**.

---

## Cómo Crear un Nuevo Post

### 1. Crear el archivo Markdown

```bash
cd ~/travel-station/blog/content/posts/
nano nombre-del-post.md

---
title: "Título del Post"
date: 2026-04-03T16:40:00+02:00
draft: false
tags: ["linux", "blog"]
showToc: true
---

Contenido del artículo…


bash ~/travel-station/scripts/preview_blog.sh


http://localhost:1313


bash ~/travel-station/scripts/deploy_blog.sh

docs/posts/preparativos-tecnicos-australia/index.html

Conclusión

Para escribir en Hugo:

    Siempre edita en content/posts/

    Nunca edites en docs/

    Usa tus scripts para previsualizar y desplegar

    Deja que Hugo genere la salida final

Con este flujo, el blog se mantiene limpio, reproducible y sin riesgo de sobrescribir contenido manualmente.
