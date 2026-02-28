# Telnet Warmup Lab – Write-up
Introduction

In this lab, I practiced the basic penetration testing approach: discovering open services, attempting access, and understanding the risks of weak authentication.

The goal was not only to gain access but also to understand why it was possible.

## Reconnaissance

First, I scanned the target system to learn which services were exposed.
```bash
nmap <target-ip>
```
The scan showed that port 23 was open and running a Telnet service.

Since an open port usually represents a possible entry point, this indicated a potential way to interact with the system.

## Service Access

Telnet provides remote terminal access to a machine.
Because it allows login interaction, I attempted to connect to the service.
```bash
telnet <target-ip>
```
After connecting, the system displayed a login prompt, confirming that authentication was required.

## Authentication

Telnet services often keep default credentials in misconfigured environments.
For this reason, I tried commonly used username and password combinations.

The login was successful using default credentials.

This demonstrates how unchanged authentication data can lead directly to unauthorized access.

## Post-Access Enumeration

After gaining access, I wanted to understand my position in the system.
```bash
pwd
```
This showed the working directory and confirmed command execution on the target machine.

## What I Learned

Open ports reveal possible attack surfaces

Telnet is insecure because it does not encrypt authentication data

Default credentials are a major real-world security risk

Reconnaissance is the most important step before exploitation
