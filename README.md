# Resploit- Understanding Telecom networks and analyzing the security of core networks in a telecom deployment
Resploit is a GUI-based penetration testing toolkit tailored for analyzing, auditing, and securing telecom core networks. Built using Python and PyQt5, it provides an intuitive interface that integrates seamlessly with powerful security tools like Nmap, Wireshark, Metasploit, and more.
Rather than serving as a generic network scanner, Resploit is crafted to assist researchers, red teamers, and telecom professionals in assessing vulnerabilities specific to telecom deployments—particularly in 5G/4G core network environments.


## Table of Contents
- [Features](#features)
- [Demo](#Demonstrations)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [Tests](#tests)
- [Deployment](#deployment)
- [Built With](#built-with)
- [Acknowledgments](#acknowledgments)

# 🛰️ Resploit - Telecom Network Pentesting Toolkit

**Resploit** is a telecom network penetration testing toolkit designed for evaluating the security posture of modern 5G core networks. Built using real-world telecom stacks like [Free5GC](https://www.free5gc.org/), this project simulates and tests vulnerabilities in the Next Generation Core (NGC) through crafted attack modules, custom analysis tools, and live demos. It aims to empower researchers, telecom engineers, and security enthusiasts with better understanding and control over 5G deployments.

---

## 🔍 Key Features

- 🧵 **Modular design** with plug-and-play testing scripts
- 🧠 **Protocol-aware fuzzing** for 5G core interfaces (NGAP, NAS, etc.)
- 🛰️ **Simulated AMF/SMF/UPF/N3IWF components** using Free5GC
- 🔐 **Security evaluation** through real-time test cases and exploits
- 📊 **Data analysis & packet capture** integrated with Wireshark and tcpdump
- 🐚 CLI-based automation and monitoring interface
- 

---

## 📦 Project Structure

```bash
Resploit/
├── core/                # Free5GC deployment files and configs
├── exploits/            # Exploitation scripts targeting specific 5G components
├── recon/               # Network scanners and information gathering tools
├── analysis/            # PCAP analyzers, logging utilities, protocol decoders
├── configs/             # YAML/JSON files for test cases and modules
├── scripts/             # Automation scripts and setup files
└── README.md
```

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Reinfosec-Resploit/Resploit.git
cd Resploit
```

### 2. Setup Free5GC Core

Ensure Docker and Golang are installed. Then follow the setup script:

```bash
cd core
./run.sh
```

This launches the AMF, SMF, UPF, NRF, AUSF, and web UI at:

- Web Console: http://127.0.0.1:5000 or http://<your_ip>:5000

### 3. Run Recon/Pentest Modules

```bash
cd recon
python3 ngap_scan.py --target 192.168.1.35
```

---
#Demonstrations
## 📺 Demonstrations

Hands-on video demos of the full project in action — including setup, core network emulation, and offensive testing.

---

### 🛰️ Complete Project Overview

A comprehensive overview of Resploit, its architecture, goals, and demo scenarios.

[![Complete Project Overview](https://drive.google.com/uc?id=1w_AfcNxaqegxe5Je0Ktx6MG4Kvf10IJB)](https://youtu.be/7aQYirUlw_c?si=-3Y0Z49CN0k6yCdb)

📹 [Watch on YouTube](https://youtu.be/7aQYirUlw_c?si=-3Y0Z49CN0k6yCdb)

---

### ⚙️ Installation and Running the 5G Core Network

Step-by-step guide to installing Free5GC and verifying service readiness.

[![Installation and Running the 5G Core Network](https://drive.google.com/uc?id=1k2pcEMQdDJTXSheVcjacoT6k4eYFe0Yk)](https://drive.google.com/file/d/1k2pcEMQdDJTXSheVcjacoT6k4eYFe0Yk/view)

📹 [Watch the Video](https://drive.google.com/file/d/1k2pcEMQdDJTXSheVcjacoT6k4eYFe0Yk/view?usp=drive_link)

---

### 🧪 Live Penetration Testing on Free5GC

Demonstrates real-time Resploit modules attacking Free5GC in a testbed.

[[Resploit Demo]![thumbnail](https://github.com/user-attachments/assets/8a00fd00-3bda-4363-b906-82b80c7610ef)
](https://drive.google.com/file/d/1pOwGlngHDP4ExZ2Uq9NIBeNU-M3mq9P8/view?usp=sharing)
*Click the image above to watch a demo video of Resploit in action.*

📹 [Watch the Demo](https://drive.google.com/file/d/1gBrkx13Oa4kM_37BFGHFZChVZCN2jcNL/view?usp=sharing)

---

## 🛠️ Technologies Used

- [Free5GC](https://www.free5gc.org/)
- Wireshark / tcpdump
- Python 3.x
- GTP, NAS, NGAP protocols
- Bash scripting

---

## 🧠 Inspiration

This project was built out of curiosity to deeply understand the 5G NGC (Next Generation Core) and highlight areas where traditional network testing doesn’t suffice in telecom environments.

---

## 📬 Contact

Have questions or feedback? Feel free to open issues or reach out via [GitHub Discussions](https://github.com/Reinfosec-Resploit/Resploit/discussions).

---

## ⚠️ Disclaimer

This toolkit is intended **only for educational and lawful research purposes**. Do **not** deploy it on production telecom networks or without proper authorization.


## Features
- **Tool Selection:** Choose from a wide range of network and security tools including Nmap, Wireshark, Metasploit, Nessus, Aircrack-ng, Burp Suite, Nikto, Hydra, John the Ripper, OpenVAS, SQLmap, Snort, and DirBuster.
- **Predefined Scan Options:** Select from various predefined scan types tailored for each tool.
- **Custom Command Arguments:** Add custom command-line arguments to suit your specific needs.
- **Output Display:** View command execution results directly within the GUI.
- **Clear Output:** Clear previous results with a single click to prepare for a new scan.

## Installation

### Prerequisites
Ensure that you have Python 3.x and `pip` installed on your system. Additionally, the necessary security tools (e.g., Nmap, Wireshark) should be installed and accessible via the command line.

### Steps
1. **Clone the Repository**
   ```bash
   git clone https://github.com/vijaykumargowdakk/resploit.git
   cd resploit
   ```

2. **Install Python Dependencies**
   ```bash
   pip install PyQt5
   ```

3. **Install Security Tools**
   Install the required security tools like Nmap, Wireshark, Metasploit, etc., depending on your needs.

## Usage

1. **Start the Application**
   ```bash
   python app.py
   ```

2. **Select a Tool**
   - Choose the desired tool from the dropdown menu.

3. **Select a Scan Option**
   - Based on the tool, select a predefined scan option.

4. **Input Details**
   - Enter the target IP address and any additional arguments required.

5. **Run the Scan**
   - Click on "Run Scan" to execute the selected command. The output will be displayed in the text area.

6. **Clear Output**
   - Use the "Clear Output" button to clear the results.

## Configuration
- **Updating Scan Options:** You can add or modify scan options by editing the `update_scan_options` method in the `ScannerApp` class.
- **Custom Tools:** To add a new tool, modify the `initUI` and `update_scan_options` methods to include the tool and its corresponding scan options.

## Contributing
We welcome contributions! To contribute:
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/your-feature-name`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/your-feature-name`).
5. Create a Pull Request.

## Tests
To run tests, you can set up unit tests for each tool and their respective commands. Add tests to ensure that the right commands are being executed and the output is correctly handled.

1. **Install Testing Framework**
   ```bash
   pip install pytest
   ```

2. **Run Tests**
   ```bash
   pytest
   ```

## Deployment
To deploy this application:
1. Ensure all dependencies are installed.
2. Package the application using a tool like PyInstaller.
   ```bash
   pyinstaller --onefile app.py
   ```
3. Distribute the generated executable to users.

## Built With
- **[Python](https://www.python.org/):** The core programming language used.
- **[PyQt5](https://riverbankcomputing.com/software/pyqt/intro):** For creating the GUI.
- **Various Security Tools:** Nmap, Wireshark, Metasploit, etc., which are leveraged for the scanning operations.
  

## Acknowledgments
- **PyQt5 Documentation** for guidance on building the GUI.
- **Open-source security tools** that make Resploit possible.

---

This README structure provides a comprehensive guide to the project and serves as a solid foundation for users, contributors, and developers alike.
