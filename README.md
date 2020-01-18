# AeonNodeScraper
## Portmanteu of Monero + Symbiote
### A symbiotic relationship exists between those that run open nodes and those that use them.
#### Modified for AEON

Scripts to maintain a database of AEON nodes with their RPC ports open

There will be so much bash it won't be funny. 

License: http://www.wtfpl.net/

Contributions welcome. All PRs will be considered. Make a branch, write it in a different language. :)


Copyright © 2017 Gingeropolous <gingeropolous@tutanota.com>
This work is free. You can redistribute it and/or modify it under the
terms of the Do What The Fuck You Want To Public License, Version 2,
as published by Sam Hocevar. See the COPYING file for more details.
Modifications Copyright © 2018 LesPristy
Released under the same fucking license.

### Original work performed by Ginger the Great, Modified for ease of use with latest v0.13.0.0+ Aeon daemons. 

# DEPENDENCIES

Developed and runs fine on Ubuntu 16.04 

Aeon daemon (aeond) in folder you specify in ``moneriote.sh`` line 9.  

A fully synced Aeond daemon running in another folder on same computer with ``--restriced-rpc`` not used and ``--rpc-bind-ip 0.0.0.0 --confirm-external-bind`` used.

A folder named what you chose on line 6 of ``moneriote.sh`` located in the same directory that node list will be sent to.

A folder named what you chose on line 15 of ``moneriote.sh`` located in the same directory that log files and HTML files will be sent to. 

curl   

netcat  

dnsutils  

Use ``sudo apt-get install dnsutils curl netcat`` to install dependencies for scraper on Ubuntu 16.04

For OSX, recommend to install ``brew install curl netcat dnstracer dnsmap dnstop``

# How to run the scraper

Start aeond and allow to fully sync the blockchain using ``--rpc-bind-ip 0.0.0.0 --confirm-external-bind``

cd to folder moneriote.sh is loated in

run ``./moneriote.sh`` and let it run until it stops. This may take a while if the daemon has synced with many daemons before.

Once it finishes, cd to folder you noted on line 6 of ``moneriote.sh`` and run ``sudo nano open.nodes.txt`` and view all the open nodes that were picked up for port 11181.

You can use this list to connect your local wallet to if desired as a "remote node" ip address. 
