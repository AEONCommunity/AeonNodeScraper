# moneriote
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

# DEPENDENCIES

Developed and runs fine on Ubuntu 16  
Bash  
Monero daemon (monerod) in /bin/  
a folder called ~/files_moneriote with the test wallet files located their. The script makes these  
a love of bash  
curl   
netcat  
dnsutils  

sudo apt-get install dnsutils curl netcat  

# Crontab entry
0,30 * * * * /home/monero/moneriote/moneriote.sh > /home/monero/files_moneriote/lastrun.log 2>&1

