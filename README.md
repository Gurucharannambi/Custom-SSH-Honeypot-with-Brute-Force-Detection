# Custom SSH Honeypot with Brute-Force Detection

## Project Overview

This project implements a custom SSH Honeypot using Python in Ubuntu.  
The system simulates an SSH service, captures incoming connection attempts, logs attacker IP addresses, and detects potential brute-force attacks using threshold-based monitoring.

The objective of this project is to understand how attackers interact with exposed services and how security monitoring systems detect suspicious activity.

---

## Features

- Listens on custom SSH port (2222)
- Captures and logs incoming connection attempts
- Tracks number of attempts per IP address
- Detects brute-force attacks using configurable threshold
- Logs alerts when suspicious behavior is detected

---

## Technologies Used

- Python 3
- Socket Programming
- Multithreading
- Ubuntu (Linux Environment)

---

## How It Works

1. The honeypot listens on port 2222.
2. When a client attempts to connect, the system:
   - Logs the attacker’s IP address
   - Increments the attempt counter
3. If an IP exceeds the defined threshold (5 attempts), a brute-force alert is triggered.
4. All activity is stored in `honeypot.log`.

---

## How to Run

### Step 1: Run the Honeypot

```bash
python3 honeypot.py
