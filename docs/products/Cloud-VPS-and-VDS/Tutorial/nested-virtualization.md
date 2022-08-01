# VPS and Nested Virtualization

Currently - Our Contabo VPS infrastructure does not support nested virtualization. This is the case, as the Hardware features that are required to run virtual machines efficiently are not present in a VPS. 

Consequently, we do not recommend running virtual machines on a VPS as performance will be subpar.  
Our *Dedicated Server* and *Virtual Dedicated Server* models on the other hand are perfectly capable of acting as a virtual machine host and support most hypervisors out of the box.  


For More, see:
+ https://contabo.com/en/dedicated-servers/   | Dedicated Servers

+ https://contabo.com/en/vds/   | VDS

Specialized operating systems for virtualization are available with Proxmox VE and XenServer. All the offered Windows Server editions come with Hyper-V support as well. Exception: If you choose a Virtual Dedicated Server and Windows Server, Hyper-V does not work.

Should you need further advice regarding our products, please let us know.
