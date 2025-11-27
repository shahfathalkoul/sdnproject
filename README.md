# SDN Learning Switch Project

## Description
This project demonstrates a simple SDN controller using Ryu that acts as a **Learning Switch**.  
The controller dynamically installs flow rules in OpenFlow switches to forward packets efficiently.

---

## Requirements
- Ubuntu 20.04/22.04
- Python 3.8 or 3.10
- Ryu 4.30
- Mininet 2.3.0d6
- Virtual switches (Open vSwitch)
- eventlet<0.33

---

## Setup

1. **Create and activate virtual environment**
```bash
python3.10 -m venv ~/ryu-venv
source ~/ryu-venv/bin/activate

# Run Controller
cd ~/sdn-project
ryu-manager simple_switch_13.py

# Run mininet 
sudo mn --topo=linear,3 --controller=remote,ip=127.0.0.1 --switch=ovsk,protocols=OpenFlow13
mininet> pingall
