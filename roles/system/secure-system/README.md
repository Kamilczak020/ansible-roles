# Secure System

This role allows you to secure your system, and should be ran after the [system setup](../setup-system).

It configures SSHD + SSHDGuard, enables UFW, installs ntpd and configures both apt and sysctl.
All settings can be adjusted in [defaults](./defaults/main.yml).