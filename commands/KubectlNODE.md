## kubectl top node my-node-name                                            
Show metrics for a given node
```
NAME             CPU(cores)   CPU%   MEMORY(bytes)   MEMORY%   
10.144.213.119   373m         19%    2480Mi          86%       
```

## kubectl describe nodes
```
Name:               10.144.213.119(worker node name)
Roles:              <none>
Labels:             arch=amd64
                    beta.kubernetes.io/arch=amd64
                    beta.kubernetes.io/instance-type=free
                    beta.kubernetes.io/os=linux
                    failure-domain.beta.kubernetes.io/region=eu-de
                    failure-domain.beta.kubernetes.io/zone=mil01
                    ibm-cloud.kubernetes.io/external-ip=159.122.178.183
                    ibm-cloud.kubernetes.io/ha-worker=true
                    ibm-cloud.kubernetes.io/iaas-provider=softlayer
                    ibm-cloud.kubernetes.io/internal-ip=10.144.213.119
                    ibm-cloud.kubernetes.io/machine-type=free
                    ibm-cloud.kubernetes.io/os=UBUNTU_16_64
                    ibm-cloud.kubernetes.io/region=eu-de
                    ibm-cloud.kubernetes.io/sgx-enabled=false
                    ibm-cloud.kubernetes.io/worker-id=kube-brkkr2of0je3ktpg9lf0-yiyicluster-default-000000dd
                    ibm-cloud.kubernetes.io/worker-pool-id=brkkr2of0je3ktpg9lf0-8c99338
                    ibm-cloud.kubernetes.io/worker-pool-name=default
                    ibm-cloud.kubernetes.io/worker-version=1.17.6_1527
                    ibm-cloud.kubernetes.io/zone=mil01
                    kubernetes.io/arch=amd64
                    kubernetes.io/hostname=10.144.213.119
                    kubernetes.io/os=linux
                    node.kubernetes.io/instance-type=free
                    privateVLAN=2218181
                    publicVLAN=2218179
                    topology.kubernetes.io/region=eu-de
                    topology.kubernetes.io/zone=mil01
Annotations:        node.alpha.kubernetes.io/ttl: 0
                    volumes.kubernetes.io/controller-managed-attach-detach: true
CreationTimestamp:  Tue, 16 Jun 2020 16:07:05 -0700
Taints:             <none>
Unschedulable:      false
Lease:
  HolderIdentity:  10.144.213.119
  AcquireTime:     <unset>
  RenewTime:       Mon, 29 Jun 2020 10:21:01 -0700
Conditions:
  Type             Status  LastHeartbeatTime                 LastTransitionTime                Reason                       Message
  ----             ------  -----------------                 ------------------                ------                       -------
  MemoryPressure   False   Mon, 29 Jun 2020 10:17:01 -0700   Thu, 25 Jun 2020 06:42:11 -0700   KubeletHasSufficientMemory   kubelet has sufficient memory available
  DiskPressure     False   Mon, 29 Jun 2020 10:17:01 -0700   Thu, 25 Jun 2020 06:42:11 -0700   KubeletHasNoDiskPressure     kubelet has no disk pressure
  PIDPressure      False   Mon, 29 Jun 2020 10:17:01 -0700   Thu, 25 Jun 2020 06:42:11 -0700   KubeletHasSufficientPID      kubelet has sufficient PID available
  Ready            True    Mon, 29 Jun 2020 10:17:01 -0700   Thu, 25 Jun 2020 06:42:11 -0700   KubeletReady                 kubelet is posting ready status. AppArmor enabled
Addresses:
  InternalIP:  10.144.213.119
  ExternalIP:  159.122.178.183
  Hostname:    10.144.213.119
Capacity:
  cpu:                2
  ephemeral-storage:  101330012Ki
  hugepages-1Gi:      0
  hugepages-2Mi:      0
  memory:             4045032Ki
  pods:               110
Allocatable:
  cpu:                1920m
  ephemeral-storage:  98573835597
  hugepages-1Gi:      0
  hugepages-2Mi:      0
  memory:             2931944Ki
  pods:               110
System Info:
  Machine ID:                 ce209ca92af24f39b72b01d6ad1d8409
  System UUID:                6E7B2519-13CB-1079-455D-6F2392FEE9A8
  Boot ID:                    b5a20651-a928-4787-8505-7b565729caaf
  Kernel Version:             4.4.0-179-generic
  OS Image:                   Ubuntu 16.04.6 LTS
  Operating System:           linux
  Architecture:               amd64
  Container Runtime Version:  containerd://1.3.4
  Kubelet Version:            v1.17.6+IKS
  Kube-Proxy Version:         v1.17.6+IKS
ProviderID:                   ibm://676e515740d84100829a08daed2a5322///brkkr2of0je3ktpg9lf0/kube-brkkr2of0je3ktpg9lf0-yiyicluster-default-000000dd
Non-terminated Pods:          (34 in total)
  Namespace                   Name                                            CPU Requests  CPU Limits  Memory Requests  Memory Limits  AGE
  ---------                   ----                                            ------------  ----------  ---------------  -------------  ---
  default                     hello-97ddc5576-655q6                           0 (0%)        0 (0%)      0 (0%)           0 (0%)         10d
  default                     hello-97ddc5576-ctf7h                           0 (0%)        0 (0%)      0 (0%)           0 (0%)         10d
  default                     hello-97ddc5576-kvjzl                           0 (0%)        0 (0%)      0 (0%)           0 (0%)         10d
  default                     hw-demo-deployment-6c965d5dcd-6nrk8             0 (0%)        0 (0%)      0 (0%)           0 (0%)         10d
  default                     hw-demo-deployment-6c965d5dcd-blv5n             0 (0%)        0 (0%)      0 (0%)           0 (0%)         10d
  default                     hw-demo-deployment-6c965d5dcd-qcdzk             0 (0%)        0 (0%)      0 (0%)           0 (0%)         10d
  default                     watson-pod-57ccbb6cd8-nksrl                     0 (0%)        0 (0%)      0 (0%)           0 (0%)         10d
  default                     watson-talk-pod-569c554fc6-n6hbp                0 (0%)        0 (0%)      0 (0%)           0 (0%)         10d
  ibm-system                  addon-catalog-source-j8hrl                      10m (0%)      100m (5%)   50Mi (1%)        100Mi (3%)     6d
  ibm-system                  catalog-operator-5fdf997564-cj6fm               10m (0%)      0 (0%)      80Mi (2%)        0 (0%)         12d
  ibm-system                  olm-operator-5bf86499cc-tqjnq                   10m (0%)      0 (0%)      160Mi (5%)       0 (0%)         12d
  kube-system                 calico-kube-controllers-5754cfb59d-w85x5        10m (0%)      0 (0%)      25Mi (0%)        3Gi (107%)     4d3h
  kube-system                 calico-node-9pmhc                               250m (13%)    0 (0%)      80Mi (2%)        0 (0%)         4d3h
  kube-system                 coredns-6567db4fff-fp8xm                        100m (5%)     0 (0%)      70Mi (2%)        400Mi (13%)    12d
  kube-system                 coredns-6567db4fff-q244f                        100m (5%)     0 (0%)      70Mi (2%)        400Mi (13%)    12d
  kube-system                 coredns-6567db4fff-z9zbl                        100m (5%)     0 (0%)      70Mi (2%)        400Mi (13%)    12d
  kube-system                 coredns-autoscaler-649976fbf4-gt9h8             20m (1%)      0 (0%)      10Mi (0%)        0 (0%)         12d
  kube-system                 dashboard-metrics-scraper-5789d44f58-8qj6d      1m (0%)       0 (0%)      10Mi (0%)        0 (0%)         12d
  kube-system                 ibm-keepalived-watcher-tskgt                    5m (0%)       0 (0%)      10Mi (0%)        0 (0%)         12d
  kube-system                 ibm-master-proxy-static-10.144.213.119          25m (1%)      300m (15%)  32M (1%)         512M (17%)     12d
  kube-system                 kubernetes-dashboard-6cfcf747-wtj54             50m (2%)      0 (0%)      100Mi (3%)       0 (0%)         4d3h
  kube-system                 metrics-server-857d7b5b77-k7m7k                 53m (2%)      148m (7%)   154Mi (5%)       404Mi (14%)    4d3h
  kube-system                 vpn-f66c45467-rmrf6                             5m (0%)       0 (0%)      5Mi (0%)         0 (0%)         12d
  razee                       featureflagsetld-controller-6cdfd49d65-9lqhz    40m (2%)      100m (5%)   75Mi (2%)        200Mi (6%)     6d23h
  razee                       managedset-controller-856b44776f-m2524          40m (2%)      100m (5%)   75Mi (2%)        200Mi (6%)     6d23h
  razee                       mongo-5757d49748-499nf                          0 (0%)        0 (0%)      0 (0%)           0 (0%)         6d19h
  razee                       mustachetemplate-controller-5b54868d5-cx8cb     40m (2%)      100m (5%)   75Mi (2%)        200Mi (6%)     6d23h
  razee                       razeedash-768d98f9bb-n2jwp                      100m (5%)     500m (26%)  80Mi (2%)        256Mi (8%)     6d19h
  razee                       razeedash-api-76c4fffbcd-nb8t2                  100m (5%)     500m (26%)  80Mi (2%)        256Mi (8%)     6d19h
  razee                       razeedeploy-delta-8587644474-lq4mj              40m (2%)      100m (5%)   50Mi (1%)        150Mi (5%)     6d23h
  razee                       redis-796f6fb456-nz7gg                          1m (0%)       500m (26%)  64Mi (2%)        256Mi (8%)     6d19h
  razee                       remoteresource-controller-589f6886fc-5fzwc      40m (2%)      100m (5%)   75Mi (2%)        200Mi (6%)     6d23h
  razee                       remoteresources3-controller-5b499b58b8-l4jbb    40m (2%)      100m (5%)   75Mi (2%)        200Mi (6%)     6d23h
  razeedeploy                 remoteresource-controller-589f6886fc-b8sq9      40m (2%)      100m (5%)   75Mi (2%)        200Mi (6%)     6d20h
Allocated resources:
  (Total limits may be over 100 percent, i.e., overcommitted.)
  Resource           Requests         Limits
  --------           --------         ------
  cpu                1230m (64%)      2748m (143%)
  memory             1688082Ki (57%)  7559456Ki (257%)
  ephemeral-storage  0 (0%)           0 (0%)
Events:              <none>
```

## kubectl get nodes -o json
 ```
{
	"kind": "Node",
	"apiVersion": "v1",
	"metadata": {
		"name": "10.144.213.119",
		"selfLink": "/api/v1/nodes/10.144.213.119",
		"uid": "030c7270-ed00-472a-9f58-c54f277e66d8",
		"resourceVersion": "337635",
		"creationTimestamp": "2020-06-16T23:07:05Z",
		"labels": {
			"arch": "amd64",
			"beta.kubernetes.io/arch": "amd64",
			"beta.kubernetes.io/instance-type": "free",
			"beta.kubernetes.io/os": "linux",
			"failure-domain.beta.kubernetes.io/region": "eu-de",
			"failure-domain.beta.kubernetes.io/zone": "mil01",
			"ibm-cloud.kubernetes.io/external-ip": "159.122.178.183",
			"ibm-cloud.kubernetes.io/ha-worker": "true",
			"ibm-cloud.kubernetes.io/iaas-provider": "softlayer",
			"ibm-cloud.kubernetes.io/internal-ip": "10.144.213.119",
			"ibm-cloud.kubernetes.io/machine-type": "free",
			"ibm-cloud.kubernetes.io/os": "UBUNTU_16_64",
			"ibm-cloud.kubernetes.io/region": "eu-de",
			"ibm-cloud.kubernetes.io/sgx-enabled": "false",
			"ibm-cloud.kubernetes.io/worker-id": "kube-brkkr2of0je3ktpg9lf0-yiyicluster-default-000000dd",
			"ibm-cloud.kubernetes.io/worker-pool-id": "brkkr2of0je3ktpg9lf0-8c99338",
			"ibm-cloud.kubernetes.io/worker-pool-name": "default",
			"ibm-cloud.kubernetes.io/worker-version": "1.17.6_1527",
			"ibm-cloud.kubernetes.io/zone": "mil01",
			"kubernetes.io/arch": "amd64",
			"kubernetes.io/hostname": "10.144.213.119",
			"kubernetes.io/os": "linux",
			"node.kubernetes.io/instance-type": "free",
			"privateVLAN": "2218181",
			"publicVLAN": "2218179",
			"topology.kubernetes.io/region": "eu-de",
			"topology.kubernetes.io/zone": "mil01"
		},
		"annotations": {
			"node.alpha.kubernetes.io/ttl": "0",
			"volumes.kubernetes.io/controller-managed-attach-detach": "true"
		}
	},
	"spec": {
		"providerID": "ibm://676e515740d84100829a08daed2a5322///brkkr2of0je3ktpg9lf0/kube-brkkr2of0je3ktpg9lf0-yiyicluster-default-000000dd"
	},
	"status": {
		"capacity": {
			"cpu": "2",
			"ephemeral-storage": "101330012Ki",
			"hugepages-1Gi": "0",
			"hugepages-2Mi": "0",
			"memory": "4045032Ki",
			"pods": "110"
		},
		"allocatable": {
			"cpu": "1920m",
			"ephemeral-storage": "98573835597",
			"hugepages-1Gi": "0",
			"hugepages-2Mi": "0",
			"memory": "2931944Ki",
			"pods": "110"
		},
		"conditions": [
			{
				"type": "MemoryPressure",
				"status": "False",
				"lastHeartbeatTime": "2020-06-29T17:12:00Z",
				"lastTransitionTime": "2020-06-25T13:42:11Z",
				"reason": "KubeletHasSufficientMemory",
				"message": "kubelet has sufficient memory available"
			},
			{
				"type": "DiskPressure",
				"status": "False",
				"lastHeartbeatTime": "2020-06-29T17:12:00Z",
				"lastTransitionTime": "2020-06-25T13:42:11Z",
				"reason": "KubeletHasNoDiskPressure",
				"message": "kubelet has no disk pressure"
			},
			{
				"type": "PIDPressure",
				"status": "False",
				"lastHeartbeatTime": "2020-06-29T17:12:00Z",
				"lastTransitionTime": "2020-06-25T13:42:11Z",
				"reason": "KubeletHasSufficientPID",
				"message": "kubelet has sufficient PID available"
			},
			{
				"type": "Ready",
				"status": "True",
				"lastHeartbeatTime": "2020-06-29T17:12:00Z",
				"lastTransitionTime": "2020-06-25T13:42:11Z",
				"reason": "KubeletReady",
				"message": "kubelet is posting ready status. AppArmor enabled"
			}
		],
		"addresses": [
			{
				"type": "InternalIP",
				"address": "10.144.213.119"
			},
			{
				"type": "ExternalIP",
				"address": "159.122.178.183"
			},
			{
				"type": "Hostname",
				"address": "10.144.213.119"
			}
		],
		"daemonEndpoints": {
			"kubeletEndpoint": {
				"Port": 10250
			}
		},
		"nodeInfo": {
			"machineID": "ce209ca92af24f39b72b01d6ad1d8409",
			"systemUUID": "6E7B2519-13CB-1079-455D-6F2392FEE9A8",
			"bootID": "b5a20651-a928-4787-8505-7b565729caaf",
			"kernelVersion": "4.4.0-179-generic",
			"osImage": "Ubuntu 16.04.6 LTS",
			"containerRuntimeVersion": "containerd://1.3.4",
			"kubeletVersion": "v1.17.6+IKS",
			"kubeProxyVersion": "v1.17.6+IKS",
			"operatingSystem": "linux",
			"architecture": "amd64"
		}
}
```
