# Shellper

Another DevOps tool box.

- [Shellper](#shellper)
  - [Features](#features)
  - [Tested](#tested)
  - [Install](#install)
  - [Uninstall](#uninstall)
  - [Use](#use)
    - [Run](#run)
    - [Include](#include)
  - [Examples](#examples)
    - [Quick LAMP install-lamp.sh](#quick-lamp-install-lampsh)
  - [Support](#support)
  - [Funding](#funding)
  - [License](#license)

[![Shellper screenshot](assets/shellper-screenshot.png)](https://www.youtube.com/watch?v=RiqMoP9DCSU)

## Features

- Simple single file script
- Time saving auto-complete commands via `rlwrap`
- Run local or install globally

## Tested

| Shellper | Distribution | Version       | Comments                         |
| -------- | ------------ | ------------- | -------------------------------- |
| `main`   | Ubuntu       | `20.04.2 LTS` |                                  |
| `0.2.1`  | Debian       | `10`          | Unattended upgrades, missing UFW |


## Install

One line install.

```bash
wget -O - https://raw.githubusercontent.com/jaitnsongara/linux-admin-toolbox/linux-admin-toolbox/install.sh | sudo bash
```

---

Alternatively you can clone the repository and run Shellper locally.

```bash
git clone https://github.com/jaitnsongara/linux-admin-toolbox/blob/linux-admin-toolbox/install.sh shellper
cd "shellper"
chmod +x shellper.sh
```

## Uninstall

1. [`rlwrap`](https://github.com/hanslub42/rlwrap) is the only dependency installed by [install.sh](install.sh). Uninstall with:

    ```bash
    sudo apt remove rlwrap
    ```

2. The installer copies a single script. This can easily be removed with:

    ```bash
    sudo rm /usr/local/bin/shellper
    ```

## Use

### Run

1. Run global

    ```bash
    shellper
    ```

    or local script

    ```bash
    ./shellper.sh
    ```

2. Start typing a command.

    > If installed via [install.sh](install.sh) `rlwrap` will provide auto-complete.

### Include

You can also include Shellper into your existing scripts or build entirely new scripts with just Shellper functions.

You can invoke the installer and include Shellper on the fly.

## Examples

### Quick LAMP [install-lamp.sh](examples/install-lamp.sh)

Provisions a performance oriented PHP web server with the following:

- Update system
- Add [Ondřej Surý](https://launchpad.net/~ondrej/+archive/ubuntu/php/) PPA for latest stable releases
- Apache
  - Enables `mod_event`
- PHP
- PHP-FPM
- Prompts the user to select MariaDB or MySQL
- memcached
- Postfix


## License

The code is licensed [MIT](https://opensource.org/licenses/MIT) and the documentation is licensed [CC BY-SA 4.0]
