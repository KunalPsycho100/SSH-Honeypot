# SSH-Honeypot
This honeypot is designed to mimic a legitimate SSH server, tricking attackers into revealing their credentials by attempting to log in. These credentials are printed for logging and analysis but access is never actually granted.
This Python script implements a basic SSH honeypot using the Paramiko library. A honeypot is a security mechanism that mimics a legitimate system to lure attackers and log their activities for analysis. This honeypot captures login attempts, including usernames and passwords, and is intended for research or educational purposes to study brute force attacks on SSH services.

Features:
SSH Server Interface: The script leverages paramiko.ServerInterface to simulate an SSH server.
Credential Logging: The script logs all SSH login attempts by capturing the provided username and password combinations.
Threaded Connections: It supports multiple simultaneous SSH connections using Python's threading module.
Custom SSH Key: The server uses an RSA key for secure communication, which can be generated or specified.

Usage:
Install dependencies:
pip install paramiko

Replace 'key' with the path to your private RSA key or generate a new one using paramiko.RSAKey.

Run the script:
python3 ssh_honeypot.py

Warning:
This script is intended for legal and ethical purposes, such as research or security awareness. Do not deploy it in any unauthorized environments.
