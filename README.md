[![add-on registry](https://img.shields.io/badge/DDEV-Add--on_Registry-blue)](https://addons.ddev.com)
[![tests](https://github.com/tyler36/ddev-laravel-reverb/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/tyler36/ddev-laravel-reverb/actions/workflows/tests.yml?query=branch%3Amain)
[![last commit](https://img.shields.io/github/last-commit/tyler36/ddev-laravel-reverb)](https://github.com/tyler36/ddev-laravel-reverb/commits)
[![release](https://img.shields.io/github/v/release/tyler36/ddev-laravel-reverb)](https://github.com/tyler36/ddev-laravel-reverb/releases/latest)

# DDEV Laravel Reverb

## Overview

This add-on integrates Laravel Reverb into your [DDEV](https://ddev.com/) project.

## Installation

```bash
ddev add-on get tyler36/ddev-laravel-reverb
ddev restart
```

After installation, make sure to commit the `.ddev` directory to version control.

## Usage

| Command | Description |
| ------- | ----------- |
| `ddev describe` | View service status and used ports for Laravel Reverb |
| `ddev logs -s laravel-reverb` | Check Laravel Reverb logs |

## Advanced Customization

To change the Docker image:

```bash
ddev dotenv set .ddev/.env.laravel-reverb --laravel-reverb-docker-image="ddev/ddev-utilities:latest"
ddev add-on get tyler36/ddev-laravel-reverb
ddev restart
```

Make sure to commit the `.ddev/.env.laravel-reverb` file to version control.

All customization options (use with caution):

| Variable | Flag | Default |
| -------- | ---- | ------- |
| `LARAVEL_REVERB_DOCKER_IMAGE` | `--laravel-reverb-docker-image` | `ddev/ddev-utilities:latest` |

## Credits

**Contributed and maintained by [@tyler36](https://github.com/tyler36)**
