Usually each programming language has it's own library repository from where libraries are downloaded. The whole system is dependent on access to that specific service.

Clojure CLI can download dependencies from any git repository and thus encourages in more distributed package management. The upside is that not everything is dependend on single library repository but the downside is that if some git repository is removed then all the builds that depend on it break.

A peer to peer network would make library distribution more resilient as there would not be a single point of failure for any widely used library. Such system would not have to be specifically run for library distribution. An existing network such as IPFS could be used.