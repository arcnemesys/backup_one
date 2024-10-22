# Introduction to Nix & NixOS

Nix is a declarative package manager, enabling users to declare a system state in configuration files.

The state of an operating system consists of many components, and declarative configuration handles the static portion of it, which is the primary focus of NixOS.

Complete system reproducibility is unfeasible but `/home` contains important configurations, dotfiles, and home-manager is a project that handles these and user level packages in the home directory.

------

# Advantages & Disadvantages

- Declarative COn