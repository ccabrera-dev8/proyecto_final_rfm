# Proyecto Final — RFM

Proyecto final desarrollado con **Symfony** (PHP), Twig y Docker.

## Stack

- **Backend:** PHP + Symfony
- **Templates:** Twig
- **Frontend:** JavaScript y CSS (AssetMapper / importmap)
- **Base de datos:** Doctrine
- **Infraestructura:** Docker + Docker Compose
- **Tests:** PHPUnit

## Requisitos

- Docker y Docker Compose
- (Alternativa sin Docker) PHP 8.2+, Composer y Symfony CLI

## Cómo ejecutar con Docker

1. Clona el repositorio:
   ```bash
   git clone https://github.com/ccabrera-dev8/proyecto_final_rfm.git
   cd proyecto_final_rfm
   ```
2. Configura las variables de entorno en `.env` (o crea `.env.local`).
3. Levanta los contenedores:
   ```bash
   docker compose up -d
   ```
4. Instala dependencias y corre las migraciones:
   ```bash
   docker compose exec app composer install
   docker compose exec app php bin/console doctrine:migrations:migrate
   ```

La aplicación queda disponible en el puerto configurado en `compose.yaml`.

## Cómo ejecutar sin Docker

```bash
composer install
symfony serve
```

## Estructura

- `src/` — código de la aplicación
- `config/` — configuración de Symfony
- `templates/` — plantillas Twig
- `migrations/` — migraciones de base de datos
- `public/` — punto de entrada
- `tests/` — pruebas (PHPUnit)
- `Dockerfile`, `compose.yaml` — configuración de Docker

## Autor

**Cesar Augusto Cabrera Marcos** — [@ccabrera-dev8](https://github.com/ccabrera-dev8)
