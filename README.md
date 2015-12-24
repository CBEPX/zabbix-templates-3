# zabbix-templates

There is an Mikrotik template. 
I'm checking: traffic on all ports, cpu load, cpu temp, motherboard temp, memory load.
It uses 1 discovery (for ifaces, cpu's), and 42 static triggers. 

Each interface discovery goes to fill 11 items with 64bit counters: port status, port admin status, bps in/out, broadcast pps in/out, multicast pps in/out, unicast pps in/out, alias of port), 
taking via mib IF-MIB

Template builded to monitor an Mikrotik CCR1036-8G-2S+, but should fit any other.

Use macros for add snmp community -> {$SNMP_COMMUNITY}

Zabbix 2.2.X
