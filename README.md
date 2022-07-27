# Whatsapp Discover

A tool for getting phone numbers of devices using Whatsapp by real time sniffing from an interface (disabled in this first version) or from a list of pcap files, which can be processed in batch

---

# Installing perl dependencies for ubuntu
### OBS

If these dependencies are not installed, **whatsapp_discover.pl** will not work.

## libnet-pcap-perl
	$ sudo apt-get install libnet-pcap-perl
## libnetpacket-perl
	$ sudo apt-get install -y libnetpacket-perl

	

	

### Note 

This code has been released as a PoC, and it does not pretend to be a hacking malicious tool. That is why real time sniffing has been disabled in this first version, to prevent from script kiddies. 

It is very easy to someone with basics knowledge of programming to enable this real time sniffing mode in this code. Also make sure that interface can get through the traffic that this script is expecting.


### Author

Deepak Daswani 

[@dipudaswani](http://twitter.com/dipudaswani)

[http://deepakdaswani.es](http://deepakdaswani.es)

### Author's github
https://github.com/deepakdaswani/whatsapp_discover

### Usage

	$ ./whatsapp_discover.pl -i interface | -f pcapfile[s]

### Example

In the example below, the numbers have been darkened with X characters for privacy reasons

	deepak@kali:~/code/whatsapp_discover$ ./whatsapp_discover.pl -f /home/deepak/pcapfiles/*.cap
	
	Whatsapp Discover v1.1  --- Deepak Daswani (@dipudaswani) 2015
	                            http://deepakdaswani.es 
	
	Parsing /home/deepak/pcapfiles/freewifi-01.cap ...
	Got 1 number! S.O: iPhone-2.11.4-5222 Mobile number: +1202XXXXXXX
	Parsing /home/deepak/pcapfiles/freewifi-02.cap ...
	Got 1 number! S.O: Android-2.11.152 Mobile number: +34616XXXXXX
	Got 1 number! S.O: Android-2.11.136 Mobile number: +34663XXXXXX
	Parsing /home/deepak/pcapfiles/freewifi-03.cap ...
	Got 1 number! S.O: BB-2.8.7345-443 Mobile number: +34695XXXXXX
	Parsing /home/deepak/pcapfiles/freewifi-04.cap ...
	Got 1 number! S.O: Symbian-2.11.173-443 Mobile number: +34660XXXXXX
	
	4 files parsed. 5 phone numbers using Whatsapp found...




