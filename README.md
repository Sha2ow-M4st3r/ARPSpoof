# ARPSpoof
Network ARP Cache Poisoning

This is a simple Python script designed to implementing ARP cache table poisoning attacks on the network. It is important to note that the script is not very fast due to the lack of multi-threading.
This script is only useful for learning network socket programming in Python and for modeling and implementing it on a small network.

NOTE1: Due to the use of raw sockets, the script must be run with root access on Linux.
NOTE2: I  think the psutil library is not installed by default on your system and you need to install it using APT or PIP.
NOTE3: This script make a one way ARP cache table poisoning attack.


In this example we make windows server 2022 system think we are the windows 10 client:

Windows 10 Client: 192.168.56.60

Windows Server 2022: 192.168.56.100

## Usage

```markdown

sudo python3 arpspoof.py -i <iface> -t <target> -s <spoofed ip>
sudo python3 arpspoof.py -i vboxnet0 -t 192.168.56.100 -s 192.168.56.60
