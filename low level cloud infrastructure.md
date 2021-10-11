Cloud infrastructure should be defined in a lower abstraction level than now.

It should mean sandboxed processes that have access to cpu cores, disk space and network interfaces. Programs that are run in the processes should not be a concern of a cloud infrastructure.

**Cloud should mean a low level operating system interface for geographically distributed hardware.**

The distribution should be made explicit and applications should be written as collections of processes. This is in contrast to distributed operating systems described in Wikipedia: [Distributed operating system - Wikipedia](https://en.wikipedia.org/wiki/Distributed_operating_system)

DNS servers, load balancers, logging services, key value stores, message queues etc. should not be part of the cloud infrastructure. They are simply processes from the cloud infrastructure point of view.

Infrastrucuture as code should mean an infrastructure definition file that specifies:
- what software should be run
- in how many processes
- in which availability zones
- what disk parititons should they mount
- what networks should the processes have access to

Each software has it's own configuration file in addition to the infrastructure definition file. When the configuration changes, the affected process should be restarted. Processes should be started and terminated accordingly to the infrastructure definition.

Speficially the processes and hardware configuration should not be defined by API calls. The configuration should be based on version controlled files and the cloud platform should allocate hardware and start and terminate processes based on the configuration file changes.

The software in the cloud processes should not require a linux distribution, i.e. a container to run. It should be a [WASM](https://webassembly.org/) binary that uses [WASI |](https://wasi.dev/) and [WebGPU](https://en.wikipedia.org/wiki/WebGPU) to access the hardware on which it is run. See [[universal sandbox]].