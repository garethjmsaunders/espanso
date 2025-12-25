# Espanso configuration

This repository contains my personal configuration for [**Espanso**](https://espanso.org/), the cross-platform text expander.

The repo is intended to be cloned directly into Espanso’s configuration directory so that all snippets and settings are version controlled and can be synchronised easily across multiple machines.

## Why this exists

This repository exists to provide a single, reliable source of truth for my Espanso setup.

It allows me to:
* Keep all text expansions and behaviour consistent across Windows and Linux on both desktop and laptop installations.
* Make changes in one place and synchronise them easily.
* Recover quickly after a rebuild or fresh install.
* Avoid manual copying, drift between machines or forgotten local changes.

This setup deliberately favours simplicity, repeatability and low maintenance over clever or complex solutions.

## What this repository contains

* `config/`
  * Global Espanso configuration files, including `default.yml`
  * Optional operating system-specific configuration files, such as `windows.yml` or `linux.yml`, if needed in future

* `match/`
  * Text expansion snippets organised into one or more YAML files
  * For example, `base.yml`, plus topic-based files such as HR or writing prompts

* `.gitattributes`
  * Ensures consistent line endings (`LF`) across Windows and Linux

* `README.md`
  * This file

There is no sensitive or private data in this repository.

## How to use this repository

### Windows

Clone this repository into:

`C:\Users<username>\AppData\Roaming\espanso`

### Linux

Clone this repository into:

`~/.config/espanso`


Espanso automatically reloads snippet changes when files are saved. If changes do not take effect immediately, or after pulling updates from Git, restart Espanso.

## Updating snippets

1. Edit the relevant YAML file
2. Commit and push changes to this repository
3. Pull the latest changes on other machines
4. Restart Espanso to apply updates

## Notes

* Espanso automatically reloads snippet changes when files are saved. If changes do not take effect immediately, or after pulling updates from Git, restart Espanso.
* The repository tracks the full Espanso configuration directory to keep behaviour consistent across machines.
* Configuration is designed to be shared across Windows and Linux, with OS-specific files added only when required.