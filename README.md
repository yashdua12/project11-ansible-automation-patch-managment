# project11-ansible-automation-patch-managment
# ANSIBLE-AUTOMATED-PATCH-MANAGEMENT

## Overview

This project is designed to automate the patch management process for Linux servers using Ansible. It ensures that your servers are up-to-date with the latest OS and security updates while maintaining application availability.

## Features

1. **Scan for Updates**: Automatically scans Linux servers for pending OS and security updates.
2. **Rolling Updates**: Applies updates in rolling batches to ensure application uptime.
3. **Conditional Reboot**: Reboots servers only when necessary, especially when OS and disk usage are high.
4. **Load Balancer Integration**: Optionally drains and reattaches nodes to a load balancer during updates.
5. **HTML Reporting**: Generates an HTML report detailing updates, reboots, and more.
6. **Slack Notifications**: Sends the HTML report to a specified Slack channel.

## Ansible Roles

1. **Precheck**: Conducts a health check before patching, including disk usage, uptime, and package cache.
2. **Patching**: Lists available updates or installs them.
3. **Reboot**: Determines if a reboot is required or forced and safely reboots the hosts.
4. **Report Role**: Collects patch results and compiles them into an HTML file.
5. **Slack**: Uploads the HTML report to a Slack channel.
6. **Main Playbook**: Includes all roles in the correct order.

## Important Points

- Ensure your private IP is listed in `inventory.yml`.
- Include your OpenSSH key content in `key.pem`, which you received when creating an EC2 instance.

## Getting Started

To get started with this project, clone the repository and follow the instructions in the playbook to configure your environment and execute the patch management process.
