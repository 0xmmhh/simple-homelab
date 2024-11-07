# My homelab

![alt text](https://github.com/0xmmhh/simple-homelab/blob/main/homelab-final.png?raw=true)

This documentation provides an overview of the homelab setup. It includes multiple components for managing media, network, and server applications, all connected to a centralized switch (TP-Link TL-SG105E) and a 4G router (Keenetic Runner 4G).

## Table of Contents

  * Overview
  * Network Topology
  * Components
      * Main PC
      * Proxmox Server
      * Raspberry Pi with Pi-hole and Unbound
      * Ubuntu Server with Docker Services
  * Usage



## Overview

This homelab is designed to provide an organized environment for managing media, server applications, and network configurations. The lab includes:

  1. Main PC: Running VMware Workstation Pro running a small Windows network for testing Active Directory, group policies, and client management.
  2. Proxmox Server on laptop: Virtualization environment hosting applications for media management.
  3. Raspberry Pi: A network management device that runs Pi-hole for ad-blocking and Unbound for DNS resolution.
  4. Ubuntu Server on laptop: An application server running multiple tools and services via Docker.

## Network Topology

The network is organized as follows:

  - Router (Keenetic Runner 4G): Acts as the gateway to the internet.
  - TP-Link TL-SG105E Switch: Central hub for connecting all devices.
  - Proxmox on laptop, PC, Raspberry Pi, Ubuntu Server on laptop: Connected to the switch to ensure seamless network communication.

## Components
1. PC running VMware Workstation Pro
- Description:

  Windows Server 2019: Provides directory services (Active Directory), DHCP, and DNS within the Windows domain.
  Windows 10 Clients: Connected to the Windows Server domain for testing policies and administration.

- Usage

  Active Directory: Manages user accounts, security policies, and device management.
  DHCP/DNS: Facilitates IP addressing and name resolution within the Windows network.

2. Proxmox Server
   - Homarr: Dashboard for monitoring and managing other applications.
   - Kavita: Self-hosted reading server.
   - Plex: Media server for streaming movies, music, and photos.
   - qBittorrent: Torrent client for managing downloads.
   - Tautulli: Monitoring tool for Plex media server.

3. Raspberry Pi with Pi-hole and Unbound
 - Description

      - Pi-hole: Network-level ad-blocking solution.
      - Unbound: DNS resolver for privacy and speed improvements.
      - Pi-hole with Unbound: Provides ad-blocking and DNS caching to all devices on the network, configured with recursive DNS via Unbound to enhance privacy.

4. Ubuntu Server with Docker Services
   - Netdata: Real-time monitoring of system performance.
   - draw.io: Diagramming tool for network design and documentation.
   - Mealie: Self-hosted recipe manager.
   - Cyberchef: Tool for data manipulation and transformation.
   - Firefly III: Personal finance management tool.


This setup provides a robust foundation for learning and experimenting with server management, network configurations, and self-hosting applications. Each component in this homelab serves a distinct purpose, from media management to network privacy, making it a versatile environment for both practical use and educational purposes.
