Beginner-friendly Linux system security and hardening notes with practical commands, user management, permissions, SSH security, firewall concepts, and security best practices.
# Linux System Security Basics

## Overview

This repository documents fundamental Linux security and system hardening concepts studied as part of my cybersecurity learning. The project focuses on user management, file permissions, SSH security, firewall configuration, password policies, and secure system administration practices commonly used in Linux environments.

## Objectives

* Understand Linux user and group management
* Learn file and directory permission models
* Explore SSH security configuration
* Study firewall concepts using UFW
* Review secure password practices
* Document basic Linux hardening techniques

## Linux User Management

Create a new user:

```bash
sudo adduser analyst
```

Add the user to the sudo group:

```bash
sudo usermod -aG sudo analyst
```

List users:

```bash
cat /etc/passwd
```

## File Permissions

Check permissions:

```bash
ls -l
```

Change file permissions:

```bash
chmod 644 report.txt
```

Change ownership:

```bash
chown analyst:analyst report.txt
```

## SSH Security

Edit SSH configuration:

```bash
sudo nano /etc/ssh/sshd_config
```

Recommended hardening settings:

* Disable root login
* Use key-based authentication
* Disable password authentication when keys are configured
* Change the default SSH port (optional)

Restart SSH service:

```bash
sudo systemctl restart ssh
```

## Firewall (UFW)

Enable firewall:

```bash
sudo ufw enable
```

Allow SSH:

```bash
sudo ufw allow 22/tcp
```

Check firewall status:

```bash
sudo ufw status
```

## Password Security

Set password expiration:

```bash
sudo chage -M 90 analyst
```

Lock a user account:

```bash
sudo passwd -l analyst
```

Unlock a user account:

```bash
sudo passwd -u analyst
```

## Basic Security Checklist

* Keep the operating system updated
* Remove unused services
* Use strong passwords
* Enable a firewall
* Disable unnecessary root access
* Monitor authentication logs
* Backup important data regularly

## Learning Outcome

This project helped me understand the fundamentals of Linux security, secure user management, file permissions, SSH configuration, firewall management, and basic system hardening practices used in cybersecurity and system administration environments.
