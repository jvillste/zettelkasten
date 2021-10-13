Cloud infrastructure should be defined in a lower abstraction level than now.

It should mean sandboxed processes that have access to cpu cores, memory, disk space and network interfaces. Programs that are run in the processes should not be a concern of the cloud infrastructure.

**Cloud should mean a low level operating system interface for geographically distributed hardware.**

The distribution should be made explicit and applications should be written as collections of processes. This is in contrast to  [distributed operating systems](https://en.wikipedia.org/wiki/Distributed_operating_system) described in Wikipedia.

DNS servers, load balancers, logging services, key value stores, message queues etc. should not be part of the cloud infrastructure. They are simply processes from the cloud infrastructure point of view.

Infrastrucuture as code should mean an infrastructure definition file that specifies:
- what software should be run
- in how many processes
- in which availability zones
- what disk partitions should be available
- what networks should the processes have access to
- how much memory should be made available

The cloud infrastructure should provide minimal API for making state changes such as replacing a configuration file or starting and stopping process. There could then be multiple different planner implementations that create an API call plan based on differences between two infrastructure definition file versions.

Each software has it's own configuration file in addition to the infrastructure definition file. When the configuration changes, the affected process should be restarted. Processes should be started and terminated accordingly to changes to the infrastructure definition.

The software in the cloud processes should not require a linux distribution, i.e. a container to run. It should be a [WASM](https://webassembly.org/) binary that uses [WASI](https://wasi.dev/) and [WebGPU](https://en.wikipedia.org/wiki/WebGPU) to access the hardware on which it is run. See [[universal sandbox]].
