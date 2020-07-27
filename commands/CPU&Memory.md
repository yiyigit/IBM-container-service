## CPU
- CPU: Compute Processor. Dual/Quad CPU --> per CPU has 4 cores
- Normal CPU usage from the OS is measured in cumulative CPU time used.
- Limits and requests for CPU resources are measured in cpu units. 
One cpu, in Kubernetes, is equivalent to 1 vCPU/Core for cloud providers and 1 hyperthread on bare-metal Intel processors.
The expression 0.1 is equivalent to the expression 100m, which can be read as "one hundred millicpu"
109m = 108113366n
`10^6`
- The CPU resource is measured in CPU units. One CPU, in Kubernetes, is equivalent to:
	- 1 AWS vCPU
	- 1 GCP Core
	- 1 Azure vCore
	- 1 Hyperthread on a bare-metal Intel processor with Hyperthreading
- Fractional values are allowed. A Container that requests 0.5 CPU is guaranteed half as much CPU as a Container that requests 1 CPU. You can use the suffix m to mean milli. For example 100m CPU, 100 milliCPU, and 0.1 CPU are all the same. Precision finer than 1m is not allowed.

## Memory
- Limits and requests for memory are measured in bytes. 
- You can express memory as a plain integer or as a fixed-point integer using one of these suffixes: E, P, T, G, M, K. You can also use the power-of-two equivalents: Ei, Pi, Ti, Gi, Mi, Ki. For example, the following represent roughly the same value: 128974848, 129e6, 129M, 123Mi
64MiB (2^26 bytes) 

## Kubernetes related components
- "Kubelet": The daemon that runs on every kubernetes node and controls pod and container lifecycle, among many other things.
- "cAdvisor": An open source container monitoring solution which only monitors containers, and has no concept of kubernetes constructs like pods or volumes.
- "Summary API": A kubelet API which currently exposes node metrics for use by both system components and monitoring systems.
- "CRI": The Container Runtime Interface designed to provide an abstraction over runtimes (docker, rkt, etc).
- "Core Metrics": A set of metrics described in the Monitoring Architecture whose purpose is to provide metrics for first-class resource isolation and utilization features, including resource feasibility checking and node resource management. "Resource": A consumable element of a node (e.g. memory, disk space, CPU time, etc).
- "First-class Resource": A resource critical for scheduling, whose requests and limits can be (or soon will be) set via the Pod/Container Spec.
- "Metric": A measure of consumption of a Resource.
