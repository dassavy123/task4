# task4 on CYBERSECURITY 


check if ufw is available or not 
COMMAND- 
sudo  ufw status 
if result : coomand not found 
COMMAND- 
sudo apt update 
sudo apt install ufw -y

Enable ufw ->>>
COMMAND -
sudo ufw allow SSH
sudo ufw enable 

check rules 
add basic rules ->>>
COMMAND -
sudo ufw allow 80 -- HTTP 
sudo ufw allow 443 - HTTPS 
sudo ufw allow 8080/tcp - TCP 

(3) Add a rule to block inbound traffic on a specific port (e.g., 23 for Telnet)
sudo ufw deny 23 ---- TELNET 

Add rule to allow SSH (port 22) if on Linux.
COMMAND- 
sudo ufw allow openSSH
sudo ufw allow Apache 
sudo ufw allow from 192.168.1.100
sudo ufw allow from 192.168.1.0/24
sudo ufw allow from 192.168.1.100 to  any port 22 


check all rules and status 
COMMAND - sudo ufw status 



SUMMARIZE HOW FIREWALL FILTERS TRAFFIC 

🔍 Inspection – The firewall examines incoming and outgoing packets based on rules.

🚦 Rules/Policies – It checks source IP, destination IP, port, and protocol against its rule set.

✅❌ Decision – If traffic matches an allow rule, it passes; if it matches a deny rule, it’s blocked.

🔄 Direction control – Firewalls filter inbound (from outside to inside) and outbound (from inside to outside) traffic.

🛡️ Types of filtering:

Packet filtering – Allows/blocks based on headers (IP, port, protocol).

Stateful inspection – Tracks active connections and ensures packets belong to a valid session.

Application-level filtering – Inspects application data (e.g., HTTP requests).

