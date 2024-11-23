import os
import platform
import subprocess

def system_info():
    print("Linux Kernel System Information:")
    print("---------------------------------")
    print(f"Kernel Version: {platform.release()}")
    print(f"Operating System: {platform.system()}")
    print(f"Architecture: {platform.machine()}")
    print(f"Hostname: {platform.node()}")
    uptime = subprocess.check_output("uptime -p", shell=True).decode().strip()
    print(f"Uptime: {uptime}")
    logged_users = subprocess.check_output("who | wc -l", shell=True).decode().strip()
    print(f"Logged-In Users: {logged_users}")

if __name__ == "__main__":
    system_info()
