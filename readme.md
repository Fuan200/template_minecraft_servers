# Template Minecraft Servers

Template Minecraft Servers is a Docker/Docker Compose template for starting a Minecraft server quickly.

The goal is to keep separate, easy-to-copy server templates for the most used mod loaders:

* Forge
* Fabric
* NeoForge
* Quilt

## Requirements

* A Server
* Docker
* Docker Compose

## Quick Start

Choose the loader you want to run, enter its folder, and start the server with Docker Compose.

### Forge

```bash
cd forge
docker compose up -d --build
```

### Fabric

```bash
cd fabric
docker compose up -d --build
```

The server listens on port `25565` by default.

## Managing The Server

View logs:

```bash
docker compose logs -f
```

Stop the server:

```bash
docker compose down
```

Restart the server:

```bash
docker compose restart
```

## Adding Mods

Put mod `.jar` files in the loader's `mods/` directory.

Example:

```bash
fabric/mods/geckolib-fabric-1.20.1-4.8.4.jar
forge/mods/geckolib-forge-1.20.1-4.8.4.jar
neoforge/mods/geckolib-neoforge-1.20.1-4.4.9.jar
quilt/mods/geckolib-fabric-1.20.1-4.2.3.jar
```

Restart the server after adding, removing, or updating mods.

## Configuration

Common files are mounted into the container so they can be edited directly from the host:

- `server.properties`
- `ops.json`
- `whitelist.json`
- `banned-ips.json`
- `banned-players.json`
- `mods/`
- `config/`
- `world/`

For Forge, `user_jvm_args.txt` is also mounted and can be used to adjust JVM arguments.

### Notes

- Default Minecraft version in the existing templates is `1.20.1`.
- Default Java image is `eclipse-temurin:17-jdk`.
