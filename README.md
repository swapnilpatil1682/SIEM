# Application level S.I.E.M. (Security information and event management) Monitoring.   


A way to check wether events are arriving is using one of these search terms:

|tstats c where index=* host="YourHostName*" by index. 
(If that yields some events, look in the list of indexes, wether your index is there)

|tstats c where index=my_index and see if that yields a count other than 0.

|tstats c where index=my_index by index sourcetype source host (to get more detailed information per index sourcetype source and host)

tstats count where index=my_index host=YourHostName by host index sourcetype source
(if you know the forwarder host name.)
