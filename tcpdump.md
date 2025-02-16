# Basic tcpdump Filters

# Capture All Traffic
tcpdump -i eth0

# Capture Traffic to and from a Specific Host
tcpdump -i eth0 host 192.168.1.1

# Capture Traffic on a Specific Port
tcpdump -i eth0 port 80

# Capture Only TCP Traffic
tcpdump -i eth0 tcp

# Capture and Save Traffic to a File
tcpdump -i eth0 -w capture.pcap

# Read Traffic from a Saved File
tcpdump -r capture.pcap

# Capture Traffic from a Specific Network
tcpdump -i eth0 net 192.168.1.0/24

# Capture Only UDP Traffic
tcpdump -i eth0 udp

# Capture Traffic with Specific Flags (e.g., SYN)
tcpdump -i eth0 'tcp[tcpflags] & tcp-syn != 0'

# Capture Traffic to and from a Specific Host and Port
tcpdump -i eth0 host 192.168.1.1 and port 443
