# Fedora Linux Web Services Configuration (Project 13-4)

## Overview
This project demonstrates the installation, configuration, testing, and permission handling for both Apache (`httpd`) and Nginx web servers on Fedora Linux.

## Key Objectives & Lab Questions
1. **Apache Default State:** Not installed by default on Fedora Workstation.
2. **Apache Configuration:**
   - **DocumentRoot:** `/var/www/html`
   - **DirectoryIndex:** `index.html`
   - **Process User/Group:** `apache:apache`
3. **Permissions & Access Control:**
   - Demonstrated that changing file permissions to `640` restricts read access from the `others` category, generating a `403 Forbidden` error.
   - Resolved access by changing the file group ownership to `apache` (`chgrp apache /var/www/html/index.html`).
4. **Nginx Configuration:**
   - **Port:** Listens on port `80` by default.
   - **DocumentRoot:** `/usr/share/nginx/html`
   - **Process User:** `nginx`

## Verification
- Inbound HTTP traffic allowed via `firewall-cmd --add-service=http --permanent`.
- Verified active web serving across both servers from host browser (`http://10.0.0.210`).




