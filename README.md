# Estructura del Proyecto Vaultwarden 
```
├── docker-compose.yml       # Configuración de Docker
├── .env.example             # Variables de entorno (plantilla)
├── Caddyfile                # Configuración de HTTPS
├── data/                    # Datos persistentes de Vaultwarden 
├── caddy_data/              # Certificados SSL
└── README.md                # Documentación
```
## Carpetas Clave:
data/: Almacena la base de datos y configuraciones (no versionar).

caddy_data/: Certificados SSL automáticos (no versionar).

## Buenas Prácticas:

Seguridad:

Usa HTTPS obligatoriamente.

Genera ADMIN_TOKEN fuerte en .env.

## Comandos Útiles:
`Acción:`	`Comando:`

`Reiniciar servicios`	`docker-compose restart`

`Ver logs`	`docker-compose logs -f`

`Detener todo`	`docker-compose down`

`Probar SMTP`	`telnet smtp.gmail.com 587`

## Generar el Admin Token (Clave de Administración):

1.Ejecuta en tu terminal:
openssl rand -base64 48

2.Guárdala en tu .env:
ADMIN_TOKEN=tu_clave_generada

## ¿Para qué sirve el Caddyfile en este proyecto?

El Caddyfile es el corazón de la configuración de Caddy, un servidor web moderno que simplifica la gestión de HTTPS y actúa como proxy inverso. 

![Logo](https://static.vecteezy.com/system/resources/previews/008/386/329/non_2x/ar-or-ra-letter-logo-design-vector.jpg)