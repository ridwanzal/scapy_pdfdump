# scapy_pdfdump
This is a simple guide how to use scapy to read capture file and visualize the data and dump in pdf document format.
* The first thing to do
* Install Python 3 via package
* Then, install scapy, follow the instruction here https://thepacketgeek.com/scapy-p-02-installing-python-and-scapy/
* Before we begin you need to install *latex editor* like gummi. Type in your console    
```
# apt-get install gummi
```
. we can start our project
```
root@user # scapy
WARNING: No route found for IPv6 destination :: (no default route?). This affects only IPv6
INFO: Please, report issues to https://github.com/phaethon/scapy
WARNING: IPython not available. Using standard Python shell instead.
Welcome to Scapy (3.0.0)
>>> 
```
. The first thing to do is to make a variable that contain our read capture file 
. Example : **variable_name=rdpcap("path/to/the/capture/file")
```
>>> a=rdpcap("/home/ridwanzal/scapy2/uji5.pcapng")
WARNING: PacketNGReader: Unparsed block type 5/#5
```
. You'll get a warning, but it's ok. Next you can view the brief summary of your data
```
>>> a
<uji5.pcapng: TCP:66575 UDP:26389 ICMP:129 Other:11371>
```
. The last we need to visualize the data using pdfdump 
. Example : **variablename[packetline_capture].pdfdump("/path/to/the/pdf/file")
```
>>> a[546].pdfdump("/home/ridwanzal/scapy2/hasil2.pdf")
```

You can see the result in repository **hasil2.pdf**


###Thank you - M. Ridwan Zalbina
