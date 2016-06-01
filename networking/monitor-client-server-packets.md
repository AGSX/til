# Debugging using TCPDump for Client-Server Problem

This is a short-guide in tracing network behavior between 2 hosts. If you run out of options in debugging at the application level, this is good for debugging at the network-level.

```
(At the client) # tcpdump -ni any host <Server IP> -w /tmp/client_tcpdump.pcap
(At the server) # tcpdump -ni any host <Client IP> -w /tmp/server_tcpdump.pcap
```

You can read the outputs in text using tshark.

```
$ tshark -r client_tcpdump.pcap
```
