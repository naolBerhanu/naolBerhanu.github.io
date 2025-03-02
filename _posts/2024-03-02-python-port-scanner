title: "Building a Simple Port Scanner in Python"
## Introduction
Port scanning is a fundamental technique in cybersecurity used to discover open ports on a target system. This information can help security professionals identify potential vulnerabilities in a network. In this article, we'll create a simple Python-based port scanner using the `socket` and `threading` libraries.

---

## **The Python Port Scanner**
Here's the full Python script for a basic multi-threaded port scanner:

```python
import socket
import threading

def scan_port(target, port):
    """Attempts to connect to a specific port on a target IP."""
    try:
        with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
            s.settimeout(1)
            result = s.connect_ex((target, port))
            if result == 0:
                print(f"[+] Port {port} is open")
    except Exception as e:
        print(f"Error scanning port {port}: {e}")

def port_scanner(target, ports):
    """Scans a list of ports on the target host using multiple threads."""
    print(f"Scanning {target}...")
    threads = []
    
    for port in ports:
        thread = threading.Thread(target=scan_port, args=(target, port))
        thread.start()
        threads.append(thread)
    
    for thread in threads:
        thread.join()
    
    print("Scan complete!")

if __name__ == "__main__":
    target_ip = input("Enter target IP: ")
    port_range = range(1, 1025)  # Scanning the first 1024 well-known ports
    port_scanner(target_ip, port_range)
```

---

## **How It Works**
1. **`scan_port(target, port)`**: Tries to connect to a given port on the target IP and checks if it’s open.
2. **`port_scanner(target, ports)`**: Uses multi-threading to scan multiple ports simultaneously, improving efficiency.
3. **User Input**: The script prompts the user for a target IP address and scans ports from 1 to 1024.
4. **Multi-threading**: Enhances performance by running multiple port checks in parallel.

---

## **Running the Script**
To run this script:
1. Install Python if you haven’t already.
2. Save the script as `port_scanner.py`.
3. Open a terminal and run:
   ```bash
   python port_scanner.py
   ```
4. Enter the target IP when prompted.

---

## **Legal & Ethical Considerations**
⚠ **Important:** Port scanning without permission is illegal in many jurisdictions. Ensure you have explicit authorization before scanning any system that you do not own.

---

## **Conclusion**
This simple port scanner is a great starting point for understanding network security. It can be expanded to include features like service detection, banner grabbing, or integration with tools like `nmap`. Happy ethical hacking! 🛡️
