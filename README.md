# 🛰️ QEMU-VMs-Manager
> **A Professional Bash-Based Virtualization Framework for Automated KVM/QEMU Orchestration.**

`QEMU-VMs-Manager` is a robust infrastructure tool designed for rapid, headless deployment of virtualized environments. It simplifies the complexity of KVM/QEMU management by automating image provisioning, disk resizing, and **Cloud-Init** metadata injection.

---

## ⚡ Key Features

* **Automated Cloud-Image Fetching:** Built-in support for Ubuntu (22.04/24.04), Debian (11/12), Fedora 40, and CentOS Stream 9.
* **Hardware Acceleration:** Leverages KVM (`-accel kvm`) for near-native CPU performance.
* **Cloud-Init Automation:** Automatically generates ISO metadata for automated user provisioning and SSH configuration.
* **Strict Resource Validation:** Integrated checks for port availability (23-65535) and system RAM/CPU thresholds.
* **Non-Destructive Cleanup:** Automated `trap` protocols to ensure temporary resources (Seed ISOs) are purged on script exit.

---

## 🛠️ Technical Specifications

The manager is designed for high-performance testing and staging, with default configurations optimized for modern workloads:

| Component | Specification |
| :--- | :--- |
| **Architecture** | `x86_64` |
| **Default Profile** | 2 vCPUs | 2048MB RAM |
| **Storage Interface** | `virtio-blk-pci` (High-throughput I/O) |
| **Networking** | User-mode stack with automated host-to-guest port forwarding |

---

## 📥 Installation & Setup

### 1. Requirements
Ensure your host system (Ubuntu/Debian recommended) has the necessary virtualization binaries:

``sudo apt update && sudo apt install -y qemu-kvm libvirt-daemon-system libvirt-clients bridge-utils cloud-image-utils curl``

### 2. Deployment
To use the Qemu-VMs-Manager, do the following things.

# Clone the repository (Important)

``git clone [https://github.com/ibrahim234105-creator/Qemu-VMs-Manager.git](https://github.com/ibrahim234105-creator/Qemu-VMs-Manager.git)``

``cd Qemu-VMs-Manager``

``chmod +x vm.sh``

### Launch the interactive manager
``./vm.sh`` or ``bash vm.sh``

# 🖥️ Usage Guide
### Upon execution, the FeatherPlayz Management Console will guide you through:
1) OS Selection: Choose from a list of verified Cloud-Images.
2) Resource Allocation: Define custom RAM, CPU cores, and storage size.
3) Port Mapping: Assign a host port for remote SSH access to the guest.
4) Automated Boot: The script handles the download, image resizing, and KVM launch in a single workflow.

# 🔬 Development & Research Focus
****This project is currently utilized for:
Benchmarking Hypervisor Overhead on Ubuntu-latest kernels.
Testing Distributed System Node Stability in isolated virtual networks.
Educational research into Linux Kernel Module interaction within QEMU environments.
POWERED BY FEATHERPLAYZ © 2026 FusionNodes Infrastructure Research Lab****





