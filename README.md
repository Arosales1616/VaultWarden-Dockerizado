# Estructura del Proyecto Vaultwarden 

├── docker-compose.yml       # Configuración de Docker
├── .env.example             # Variables de entorno (plantilla)
├── Caddyfile                # Configuración de HTTPS
├── data/                    # Datos persistentes de Vaultwarden 
├── caddy_data/              # Certificados SSL
└── README.md                # Documentación

## Carpetas Clave:
data/: Almacena la base de datos y configuraciones (no versionar).

caddy_data/: Certificados SSL automáticos (no versionar).

## Buenas Prácticas:
No versionar:

Añade data/, caddy_data/ y .env a .gitignore.

Seguridad:

Usa HTTPS obligatoriamente.

Genera ADMIN_TOKEN fuerte en .env.

## Comandos Útiles:
Acción:	Comando:
Reiniciar servicios	docker-compose restart
Ver logs	docker-compose logs -f
Detener todo	docker-compose down
Probar SMTP	telnet smtp.gmail.com 587

## Generar el Admin Token (Clave de Administración):

1.Ejecuta en tu terminal:
openssl rand -base64 48

2.Guárdala en tu .env:
ADMIN_TOKEN=tu_clave_generada