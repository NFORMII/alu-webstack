# Web Infrastructure Project: SSL Termination and Subdomain Audit

## Overview

This project sets up SSL termination using HAProxy for a website, along with a script to audit subdomains of the domain. The SSL certificates are managed using **Certbot** (Let’s Encrypt), and HAProxy is configured to handle both HTTP-to-HTTPS redirection and secure SSL connections. The subdomain audit checks the DNS records for common subdomains.

## Features

- **SSL Termination**: Uses HAProxy to accept SSL traffic on port 443 and forward it to backend servers.
- **HTTP to HTTPS Redirection**: Redirects all HTTP traffic to HTTPS to ensure secure connections.
- **Subdomain Audit**: A script to check the DNS records of common subdomains.
- **Automatic Certificate Renewal**: Certbot is configured to automatically renew SSL certificates before they expire.

## Project Files

### 1. `0-world_wide_web` (Subdomain Audit Script)

This is a Bash script to check the DNS records of subdomains for the provided domain.

#### Usage:

```bash
chmod +x 0-world_wide_web
./0-world_wide_web girbong.tech
