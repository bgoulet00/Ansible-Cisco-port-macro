# Ansible-Cisco-port-macro
create port macro on cisco switch using ansible

I wasn't able to find any other examples of someone being successful with this so hopefully these scripts help

macro is a multiline config that does not return a device prompt between commands.  this confuses ansible
the workaround is to send a single config line that contains \r carriage return characters between the commands

the first example script embeds the carriage returns (\r) in a single long string to be transmitted to the device
this long string can become difficult to read and work with

the second example uses the ansible multiline feature, making it much prettier and easier to work with
