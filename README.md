Splunk Universal Forwarder Install

Should be compatible with Ubuntu and Debian. Tested with Ubuntu 14.01
All credits to https://github.com/aplura/Tango 

Script modified to be compatible with Modern Honey Network
In my setup the Universal forwarder forwards to the Universal forwarder on the MHN server. This UF will forward all to Splunk with index "honeypot"
Works together with the "Tango Honeyport Intelligence" Splunk app. Cowrie json logging includes session id which is very useful for analysis and building dashboards.

Updates UMASK of cowrie startup script to make the log files readable for splunk.


Installation:

git clone https://github.com/KrisBogaerts/install_splunk-uforwarder_cowrie.git /tmp/uf
chmod +x /tmp/uf/install_splunk-uf_cowrie.sh
cd /tmp/uf/
./install_splunk-uf_cowrie.sh


Input needs to be created in the Universal forwarder on the MHN server
add: [splunktcp://:9997]
to: /opt/splunkforwarder/etc/system/local/inputs.conf 



