---
title: "Bitácora Técnica: Despliegue ODROID C2"
date: 2026-04-02T17:30:00+02:00
draft: false
tags: ["cli", "linux", "australia"]
showToc: true
---

## Guía Rápida de Comandos (CLI)

Para no olvidar la gestión del sistema durante el viaje, estos son los alias activos:

### Red y Seguridad
- `vpn on` : Levanta el túnel WireGuard (Cloudflare).
- `vpn off` : Apaga el túnel.
- `vpn status` : Muestra el tráfico y handshake.

### Gestión del Blog
1. **Previsualizar local:** `bash ~/travel-station/scripts/preview_blog.sh`
2. **Publicar cambios:** `bash ~/travel-station/scripts/deploy_blog.sh`

## Estado del Hardware
El **Guardián** (Python) reporta salud en: `~/travel-station/guardian/logs/health.log`.

---
**M. Castillo - Privacy Tools**
2026
