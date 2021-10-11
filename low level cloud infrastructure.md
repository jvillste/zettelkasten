Cloud infrastructure should stay in lower abstraction level.

It should mean sandboxed processes, disk space and network interfaces. Programs that are run in the processes should not be a concern of a cloud provider.

DNS servers, load balancers, logging services, key value stores, message queues etc. should not be part of the cloud infrastructure. They are simply processes from the cloud infrastructure point of view.