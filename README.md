# Clean Starter for the latest WordPress Installation for Local development of themes and plugins of WordPress

## Do not use it in production with this ENV settings in docker-compose.yml

Run the docker-compose commands to build destroy and rebuild this installation:

```
docker-compose up
docker-compose down
docker-compose rm
docker ps
docker ps -a
docker image ls
docker images
docker network ls
docker system prune
docker system prune -a
```

These above commands will need some knowledge of basic docker

## This installation uses a clean WordPress \_underscores theme

The theme files are in the `/wp-content` folder.
This folder will be syncronized with the docker container `wp-content` folder.

Any other subfolders eg. plugins, uploads, etc will be synced as well

## How to begin!

Run docker-compose command while inside the root folder containing the docker-compose.yml file:

`docker-compose up`

When the command finishes running visit `http://localhost:7777` to finish the WordPress initial installation and setup.

## Stop containers

If you want to stop containers:

`docker ps`

`docker stop [wordpress container ID]`

`docker stop [database container ID]`

# What to do after you stop the running containers?

Just start the containers again.

Inspect the containers to find out their IDs:

`docker ps -a`

Then start them again:

`docker start [wordpress container ID]`

`docker start [database container ID]`

Start, stop and restart your project any time to develop.

When you destroy all containers and images (including database) you will need to start anew and configure WP initil installation again.

Destroy the containers and images for a sresh start:

`docker system prune -a`

Otherwise just go back to your web browser address `http://localhost:7777` and login to continue development.

## Additional info for Prepros App owners to proces Sass files.

Prepros project config file is in `/wp-content/themes/dms-wptheme/prepros.config`.

This file will help compile scss files from the project and sync everything live while developing.

**_Happy WordPressing_**
