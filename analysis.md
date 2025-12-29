create a file 

nano reports/analysis.md

content 
# Network Traffic Analysis – Investigation Report

## Analyst
Balaji

## Objective
To capture, analyze, and detect malicious network activity using terminal-based tools and IDS mechanisms.

---

## Tools Used
- [tcpdump](chatgpt://generic-entity?number=0)
- [Wireshark](chatgpt://generic-entity?number=1) (tshark)
- [Snort](chatgpt://generic-entity?number=2)

---

## Phase 1: Traffic Capture

### Command Used
```bash
sudo tcpdump -i eth0 -w captures/traffic.pcap


packet summery 

tshark -r captures/traffic.pcap
Dns traffic 

tshark -r captures/traffic.pcap -Y "dns"

http request 

tshark -r captures/traffic.pcap -Y "http.request"

suspecious behaviour identify the top talkers 

tshark -r captures/traffic.pcap -T fields -e ip.src | sort | uniq -c | sort -nr
detect TCP syn Scans 

tshark -r captures/traffic.pcap -Y "tcp.flags.syn == 1 and tcp.flags.ack == 0"

Detect SSH Brute Force 

tshark -r captures/traffic.pcap -Y "tcp.port == 22"

Detect ICMP Flood 

tshark -r captures/traffic.pcap -Y "icmp" 
RUN IDS detection 
sudo snort -i eth0 -A console -c /etc/snort/snort.conf
