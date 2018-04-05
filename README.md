# 3PAR-Brocade


#########################
##### 3PAR Array Commands #####
#########################

switchshow - shows active/passive switch status info (principle == active)

nodefind <alias> | grep -E "Remote|Local" - runs nodefind against a host alias and returns single word result if host is local or remote to the current switch

statvlun -hostsum -ni -rw -sortcol 9,inc  shows performance per host, sorts current latency in ascending order

statvlun -nodes 0 -slots 0 -ports 1 will show host/vv data usage on that port

sr<cmd> will show some historical data

showeeprom shows BIOS and OS version

showeventlog -min 20 shows system events for hte last 20 minutes

shownodeenv shows operating environment status for all nodes in the system

shownet show IP address

showuserconn shows current connected users

statpd -iter3 -sortcol 9 show disk response time and IOPS

showpd -failed -degraded -i

statvlun -iter 1 - 30 -rw -ni -<hostname> show vlun performance with R/W serparated

statport -iter 5 show R/W and queue length stats for ports

showsralertcrit shows all critical alerts on an array

removesralertcrit -pat * -f removes all alerts from an array

#########################
###### Brocade    Switches ######
#########################

alishow <hostname> shows any alias for the host, used to find what array the host is on
nodefind <arrayportwwn> will show what switch port the array is connected to
portshow <port> will show the current port status. ignore portnumber for all ports
errdump will show the running error log

#########################
###### 3PAR Patch Staging ######
#########################

Update > Update HP 3PAR OS > Next > ISO Image > Browse > Find the file > Next
Once upload is complete, hit back otherwise the patching will start.
