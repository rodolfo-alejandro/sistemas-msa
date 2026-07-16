# Sistemas MSA — Portfolio

Sitio principal de [sistemas-msa.com](https://sistemas-msa.com): presentación y enlaces a los productos en subdominios.

## Stack

- HTML / CSS / JS estático
- Docker + nginx (`nginx:1.27-alpine`)
- Host nginx hace proxy SSL → contenedor en el puerto `8093`

## Desarrollo local

```bash
docker compose up -d
```

Abrí http://localhost:8093

## Producción

En el server (`/opt/sistemas-msa`):

```bash
docker compose up -d --force-recreate
```

Nginx del host apunta `sistemas-msa.com` / `www` a `127.0.0.1:8093`. Los subdominios (`bikers.`, `gym.`, etc.) tienen configs propias y no se tocan.

## Proyectos listados

| Producto       | URL                             |
|----------------|---------------------------------|
| MSA Bikers     | https://bikers.sistemas-msa.com |
| MSA Gym        | https://gym.sistemas-msa.com    |
| MSA Empleos    | https://empleos.sistemas-msa.com|
| Reportar Salta | https://reportasalta.com        |

## Contacto

- Rodolfo Alejandro Aguirre
- Email: sistemas.msa95@gmail.com
- Tel / WhatsApp: 387 410-8192
