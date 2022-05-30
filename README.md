# tshark-snapshot
a small tool that utilizes tshark for some basic insights overview + commentary on packet captures.

A brief Pcap reader tool for fast summary output before deep dive.

this doesn't do anything you couldn't run manually, but it's handy for me so I can just get a brief snapshot of what I'm looking at before digging in.


#resources:
$ tcpdump -s 0 -n -i ethX -w /tmp/$(hostname)-$(date +"%Y-%m-%d-%H-%M-%S").pcap 

how to capture packets from inside OCP3.11 pod:
https://access.redhat.com/solutions/3480421

how to capture packets from inside OCP4 pod:
https://access.redhat.com/solutions/4569211

TCPDUMP packet capture syntax generator:
https://access.redhat.com/labs/nptcpdump/




This script is designed to run on any and all `*.pcap` files in the current working directory, and gathers the following:

- endpoints and packet loss overview

- unique endpoints by pcap

- zero-window and non-standard TCP replies (DUPs)

- TCP resets observed by pcap

