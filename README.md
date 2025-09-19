[![add-on registry](https://img.shields.io/badge/DDEV-Add--on_Registry-blue)](https://addons.ddev.com)
[![tests](https://github.com/tyler36/ddev-laravel-reverb/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/tyler36/ddev-laravel-reverb/actions/workflows/tests.yml?query=branch%3Amain)
[![last commit](https://img.shields.io/github/last-commit/tyler36/ddev-laravel-reverb)](https://github.com/tyler36/ddev-laravel-reverb/commits)
[![release](https://img.shields.io/github/v/release/tyler36/ddev-laravel-reverb)](https://github.com/tyler36/ddev-laravel-reverb/releases/latest)

# DDEV Laravel Reverb

## Overview

This add-on integrates [Laravel Reverb](https://reverb.laravel.com/) into your [DDEV](https://ddev.com/) project.

See [Laravel Reverb documentation](https://laravel.com/docs/master/reverb) for more details.

## Installation

```bash
ddev add-on get tyler36/ddev-laravel-reverb
ddev restart
```

After installation, make sure to commit the `.ddev` directory to version control.

This add-on attempts to configure Laravel for Reverb.
You can manually re-run the wizard using: `ddev artisan install:broadcasting`

## Usage

| Command | Description |
| ------- | ----------- |
| `ddev describe` | View service status and used ports for Laravel Reverb |
| `ddev logs -s web` | Check Laravel Reverb logs |

## Advanced Customization

To customize this service, remove `#ddev-generated` from `.ddev/config.laravel-reverb.yaml` before making any changes.

- To disable auto-start, comment out the `web_extra_daemons` section.
- To change reverb ports, update the `web_extra_exposed_ports` section.

> [!IMPORTANT]
> `http_port` and `https_port` are required and must be different for `ddev-router` to start.

Make sure to commit the `.ddev/config.laravel-reverb.yaml` file to version control.

## Credits

**Contributed and maintained by [@tyler36](https://github.com/tyler36)**
