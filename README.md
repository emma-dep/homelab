# Emma's Homelab

A personal Linux homelab built to develop practical experience with system
administration, networking, containers, monitoring, automation, security and
disaster recovery.

**Live portfolio:** https://emma-dep.github.io/homelab/

## Infrastructure

The lab currently consists of three primary Linux systems with different roles.

### Pandora — Core Services

Linux Mint server responsible for core self-hosted infrastructure.

- Jellyfin
- Pi-hole
- Vaultwarden
- Caddy
- Home Assistant
- Whisper
- Piper
- Automated service backups

### Demeter — Monitoring

Headless Debian server providing independent monitoring and alerting.

- Uptime Kuma
- ntfy
- Docker
- Infrastructure monitoring
- Push notifications

### Artemis — Workstation & Automation

Fedora workstation used for administration, development and media automation.

- Sonarr
- Prowlarr
- qBittorrent
- FlareSolverr
- Git
- SSH administration

## Featured Project — Backup & Disaster Recovery

I built an automated backup system for critical services running on Pandora.

The system includes:

- Dedicated external backup storage
- Service-specific Bash backup scripts
- systemd timers
- Mount-point validation
- Consistent SQLite database backups
- SQLite integrity verification
- Automatic snapshot retention
- Failure handling through systemd `OnFailure=`
- Authenticated ntfy notifications
- Independent notification infrastructure hosted on Demeter

The failure-notification path was tested using a deliberately failing disposable
systemd unit to verify the complete alert chain.

See the full case study on the portfolio website.

## Technologies

`Linux` `Fedora` `Debian` `Linux Mint` `Docker` `systemd` `Bash` `SSH`
`Git` `DNS` `Caddy` `SQLite` `UFW`

## Current Focus

Future improvements include:

- Documented disaster-recovery procedures
- Periodic restore testing
- Backup encryption at rest
- Additional off-site backups
- Expanded infrastructure documentation
- Additional portfolio case studies

## Security

This repository contains documentation and sanitized examples only.

Credentials, private keys, internal addressing, authentication secrets and other
sensitive infrastructure information are intentionally excluded.
