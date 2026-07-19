# Infraestructura segura de WordPress

Proyecto semestral de Introducción a la Ciberseguridad.

## Arquitectura

- Nginx como balanceador de carga.
- Dos instancias de WordPress.
- MariaDB como base de datos compartida.
- Redis para caché de objetos.
- Docker Compose.
- HTTPS con certificado autofirmado RSA de 4096 bits.
- TLS 1.2.
- Bloqueo de intentos fallidos.
- Modificación de la ruta de acceso administrativo.
- Integración continua con GitHub Actions.

## Servicios

- `nginx_balanceador`
- `wordpress1`
- `wordpress2`
- `mariadb`
- `redis`

## Ejecución

1. Copiar `.env.example` como `.env`.
2. Cambiar las contraseñas de ejemplo.
3. Generar el certificado y su clave privada.
4. Ejecutar:

```bash
docker compose up -d
