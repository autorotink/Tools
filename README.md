# TCPDump Training and Analysis

## Training Courses Completed
- **TryHackMe - TCPDump Room**
  - Platform: TryHackMe
  - Description: Completed hands-on exercises to learn `tcpdump` basics, filtering techniques, and packet analysis.
  - Link: [TryHackMe TCPDump Room](https://tryhackme.com/room/tcpdump)
  - Notes: This TryHackMe room gave a good introduction to tcpdump, how to capture, write, read, and filter pcaps.  

- **Antisyphon: Intro to SOC - TCPDump Lab**
  - Platform: Antisyphon - ADHD
  - Description: Participated in interactive labs to master advanced `tcpdump` usage, troubleshooting, and network security analysis.
  - Link: [Antisyphon TCPDump Lab](https://github.com/strandjs/IntroLabs/blob/master/IntroClassFiles/Tools/IntroClass/TCPDump/TCPDump.md)
  - Notes: This lab quickly ran through some of the basics, but really went into analysis, like what a HTTP GET request PowerShell script looks like.

## Skills Acquired
- Network traffic capture and analysis using `tcpdump`.
- Filtering and extracting specific information from packet captures.
- Identifying and analyzing security threats using `tcpdump`.

## Summary Table
| Command                                                           | Explanation                                                                                                                                            |
| ----------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `ip address show`                                                 | shows available network devices                                                                                                                        |
| `tcpdump -D`                                                      | shows available interfaces                                                                                                                             |
| `tcpdump -i INTERFACE`                                            | captures packets on a specific network interface                                                                                                       |
| `tcpdump -w FILE`                                                 | Writes captured packets to a file                                                                                                                      |
| `tcpdump -r FILE`                                                 | Reads captured packets from a file                                                                                                                     |
| `tcpdump -c COUNT`                                                | Captures a specific number of packets                                                                                                                  |
| `tcpdump -n`                                                      | Don't resolve IP addresses                                                                                                                             |
| `tcpdump -nn`                                                     | Don't resolve IP addresses, nor port protocols                                                                                                         |
| `tcpdump -v`                                                      | Verbose display                                                                                                                                        |
| `tcpdump -i eth0 -c 50 -v`                                        | Capture and display 50 packets listening on eth0, display them verbosely.                                                                              |
| `tcpdump -i wlo1 -w data.pcap`                                    | Capture packets listening on wlo1, and writes them to data.pcap.                                                                                       |
| `tcpdump -i any -nn`                                              | Capture packets on all interfaces and displays them on screen without domain name nor protocol resolution                                              |
| `tcpdump -i ens5 -c 5 -n`                                         | Capture and display 5 packets listening on ens5, do not resolve IP Addresses.                                                                          |
| `tcpdump host IP or tcpdump host HOSTNAME`                        | Filter packets by IP address or hostname                                                                                                               |
| `tcpdump src host IP`                                             | Filter packets by specific source host                                                                                                                 |
| `tcpdump dst host IP`                                             | Filter packets by specific destination host                                                                                                            |
| `tcpdump port PORT_NUMBER`                                        | Filter packets by port number                                                                                                                          |
| `tcpdump src port PORT_NUMBER`                                    | Filter packets by specific source port number                                                                                                          |
| `tcpdump dst port PORT_NUMBER`                                    | Filter packets by specific destination port number                                                                                                     |
| `tcpdump PROTOCOL`                                                | Filter packets by protocol (ip6, icmp, tcp, etc.)                                                                                                      |
| `tcpdump -i any tcp port 22`                                      | Listens to all interfaces, captures tcp packets to/from port 22.                                                                                       |
| `tcpdump -i wlo1 udp port 123`                                    | Listens on wlo1 and filters udp traffic on port 123.                                                                                                   |
| `tcpdump -i eth0 host example.com and tcp port 443 -w https.pcap` | Listens on eth0, for traffic with example.com that uses tcp and port 443 and write it to a file. (It's filtering https traffic related to example.com) |
| `tcpdump "tcp[tcpflags] == tcp-syn`                               | capture TCP packets with only the SYN flag set.                                                                                                        |
| `tcpdump "tcp[tcpflags] & tcp-syn != 0`                           | capture TCP packets with at least the SYN flag set.                                                                                                    |
| `tcpdump "tcp[tcpflags] & (tcp-syn\|tcp-ack) !=0"`                | capture TCP packets with at least the SYN or ACK flags set.                                                                                            |
| `tcpdump -q`                                                      | Brief packet info                                                                                                                                      |
| `tcpdump -e`                                                      | Include MAC addresses                                                                                                                                  |
| `tcpdump -A`                                                      | Print as ASCII encoding                                                                                                                                |
| `tcpdump -xx`                                                     | Display in hexadecimal                                                                                                                                 |
| `tcpdump -X`                                                      | Show in both hex and ASCII                                                                                                                             |
