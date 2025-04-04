# Uninstall Redis

This guide provides step-by-step instructions to uninstall Redis on Ubuntu. operating systems.

## Table of Contents

- [Uninstalling Redis on Ubuntu/Debian](#uninstalling-redis-on-ubuntudebian)
- [Verifying Redis Uninstallation](#verifying-redis-uninstallation)

---

## Uninstalling Redis on Ubuntu/Debian

### 1. Stop the Redis service

```sh
sudo systemctl stop redis
```

### 2. Uninstall Redis

```sh
sudo apt-get remove --purge redis-server
```

### 4. Remove unnecessary dependencies and clean cache

```sh
sudo apt-get autoremove
sudo apt-get autoclean
```

### 5.(Optional) Remove Redis data and configuration files

```sh
sudo rm -rf /var/lib/redis
sudo rm -rf /etc/redis
```

## Verifying Redis Uninstallation

### 1. Check if the Redis service is running: Run the following command to check if Redis is still running as a service:

```sh
sudo systemctl status redis
```

If Redis is uninstalled, it should show an error like "Unit redis.service could not be found."

### 2. Check if Redis is still installed: You can use the following command to check if Redis is installed:

```sh
redis-server --version
```

If Redis is uninstalled, this command should return an error like command not found.
