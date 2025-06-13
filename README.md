# my-nix-config
# Nix User Guide: Built-in Bluetooth Support and Development Packages

Welcome to this quick-start guide for Nix users! This README will help you understand how to leverage NixOS's **inbuilt support for Bluetooth** and information about some essential **inbuilt development packages** you can use for a smooth development experience.

---

## Table of Contents

- [Introduction](#introduction)  
- [Bluetooth Support in Nix](#bluetooth-support-in-nix)  
- [Using Inbuilt Development Packages](#using-inbuilt-development-packages)  
- [Sample Usage and Tips](#sample-usage-and-tips)  
- [Demo Data for Testing](#demo-data-for-testing)  
- [Helpful Resources](#helpful-resources)  

---

## Introduction

NixOS comes with incredible built-in support for Bluetooth devices and a rich ecosystem of development packages that simplify managing your development environment without conflicts. This guide assumes you are new to Nix and would like to quickly get started with Bluetooth connectivity and basic development tools.

---

## Bluetooth Support in Nix

- NixOS provides native support for Bluetooth through the `bluez` package, which includes the Bluetooth protocol stack for Linux.  
- The system configuration makes it easy to enable and manage Bluetooth services via Nix configuration files.  
- The Bluetooth service is modular and works well with the modern `systemd` system manager in NixOS.  

### How to enable Bluetooth

Add the following to your `/etc/nixos/configuration.nix`:

```nix
{
  services.bluetooth.enable = true;  # Enable the Bluetooth daemon and support
  hardware.bluetooth.enable = true;  # Enable Bluetooth kernel modules
}
