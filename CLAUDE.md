# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository implements a Tailscale Subnet Router that can be deployed on Railway. The project enables access to devices on a subnet without installing Tailscale on each individual device.

## Project Status

The project is in its initial stages. As of the initial commit, only the LICENSE and README files exist. Implementation needs to be created from scratch.

## Key Concepts

- **Tailscale**: A VPN service that creates secure networks between devices using WireGuard
- **Subnet Router**: A Tailscale feature that advertises routes to a subnet, allowing Tailscale network members to access devices on that subnet
- **Railway**: A cloud platform for deploying containerized applications

## Expected Implementation Components

When implementing this project, consider the following components:

1. **Containerization**: A Dockerfile will be needed for Railway deployment
2. **Tailscale Setup**: Configuration for running Tailscale in a container with subnet routing enabled
3. **Authentication**: Secure handling of Tailscale auth keys (likely via environment variables)
4. **Railway Configuration**: railway.json or railway.toml for deployment settings
5. **Network Configuration**: Proper setup of IP forwarding and routing rules

## Development Guidelines

Since this is a network infrastructure project:
- Prioritize security in all implementations
- Use environment variables for sensitive configuration
- Document network requirements and limitations clearly
- Consider container restart policies for reliability
- Implement proper logging for debugging network issues

## Railway Deployment Considerations

- Railway provides environment variables that should be used for configuration
- Containers in Railway are stateless, so consider this for Tailscale state management
- Railway supports both Dockerfile and Nixpacks deployments