# UBUNTU WSL2

Instructions for setting up Ubuntu WSL2 for local development.
Ubuntu LTS 20.04 is installed.

: **Update Ubuntu 20.04 to 20.10**

Steps to update Ubuntu from **lts** to **latest** is available in [windows-central](https://www.windowscentral.com/how-upgrade-ubuntu-2010-wsl-windows-10) website.

> In file **/etc/update-manager/release-upgrades** edit prompt (last line) from "lts" to "normal", then execute the following commmands in bash.

```bash
    sudo do-release-upgrade
    ! If required
    sudo apt-get-update
    sudo apt-get-upgrade
    sudo apt autoremove
```

---

## GIT

To the latest Git Repo, as by default latest ***stable*** version of git is only installed not the *latest* version.

```bash
    sudo add-apt-repository ppa:git-core/ppa
    sudo apt-get update
    sudo apt install git
```

### SSH to GitHub

---

## NODE

First **nvm** is to be installed.

```bash
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
```

Install latest vesrion of node,

```bash
    nvm install node
```

> **TODO**
How to update nvm?

---

## PYTHON

Python comes preinstalled with WSL Ubuntu, but again latest version is not available from repo, only stable version is available. To install latest version ppa/deadsnakes is to be added.

---

## RUST

Command to install Rust is directly available from [Rust-Lang Website](https://www.rust-lang.org/tools/install).

```bash
    curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

---

## JULIA

Download directly from [Julia-Lang](https://julialang.org/downloads/) website as tar ball. Extract and then use.

```bash
    wget -c https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.0-linux-x86_64.tar.gz -O /tmp/julia
    tar -xvzf /tmp/julia -C /tmp
    sudo mv /tmp/julia-[version]/ /home/[name]/.julia
    sudo ln -s /home/[user]/.julia/bin/julia /usr/bin/julia
```
