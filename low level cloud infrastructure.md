Cloud infrastructure should be defined in a lower abstraction level than now.

It should mean sandboxed processes that have access to cpu cores, disk space and network interfaces. Programs that are run in the processes should not be a concern of a cloud infrastructure.

**Cloud should mean a low level operating system interface for geographically distributed hardware.**

DNS servers, load balancers, logging services, key value stores, message queues etc. should not be part of the cloud infrastructure. They are simply processes from the cloud infrastructure point of view.

Infrastrucuture as code should mean configuration files that specify:
- what software should be run
- in how many processes
- in which availability zones
- what disk parititons should they mount
- what networks should the processes have access to

Each software has it's own configuration file in addition to the infrastructure definition file. When the configuration changes, the affected processes should be restarted and processes should be started and terminated accordingly.