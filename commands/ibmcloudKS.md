## ibmcloud ks clusters
```
OK
Name                              ID                     State    Created        Workers   Location   Version        Resource Group Name   Provider   
Katherinecluster-dal10-b3c.4x16   bs2bf4rd0nfea88qhrsg   normal   2 days ago     3         Dallas     1.18.4_1517    default               classic   
mycluster                         bpt22chs0astla2p70eg   normal   3 months ago   7         Sydney     1.16.11_1536   default               classic   
mycluster-dal12-u3c.2x4           bs2et24d0ocltoa6prng   normal   2 days ago     3         Dallas     1.18.4_1517    default               classic   
myclustergb                       bpnfngnl09bqeadlqc6g   normal   3 months ago   1         London     1.16.11_1536   default               classic   
myclusterjp                       bpnfmset021rs2ts1d8g   normal   3 months ago   3         Tokyo      1.16.11_1536   default               classic   
newJPTestCluster                  bqko03ft0vqj9jd0dpl0   normal   2 months ago   9         Tokyo      1.16.11_1536   default               classic   
yiyi-v1.15.12                     bs2gk1bd0optjm26ps4g   normal   1 day ago      2         Dallas     1.15.12_1543   default               classic   
yiyi-v1.16.11                     bs2bedod07rme18qhrqg   normal   2 days ago     3         Dallas     1.16.11_1536   default               classic   
```
## ibmcloud ks worker-pool ls --cluster yiyicluster-free
-------> cluster id
```
Kubernetes version 1.16 has removed deprecated APIs. For more information, see <http://ibm.biz/k8s-1-16-apis>
OK
Name      ID                             Flavor   Workers   
default   brkkr2of0je3ktpg9lf0-8c99338   free     1   
```

## ibmcloud ks cluster config --cluster yiyicluster-free
```
OK
The configuration for yiyicluster-free was downloaded successfully.

Added context for yiyicluster-free to the current kubeconfig file.
You can now execute 'kubectl' commands against your cluster. For example, run 'kubectl get nodes'.
```

## ibmcloud ks worker ls --cluster yiyicluster-free
```
OK
ID                                                       Public IP         Private IP       Flavor   State    Status   Zone    Version   
kube-brkkr2of0je3ktpg9lf0-yiyicluster-default-000000dd   159.122.178.183   10.144.213.119   free     normal   Ready    mil01   1.17.6_1527*   
```

## ibmcloud ks cluster get --cluster yiyicluster-free
```
Retrieving cluster yiyicluster-free...
OK
                                   
Name:                           yiyicluster-free   
ID:                             brkkr2of0je3ktpg9lf0   
State:                          normal   
Created:                        2020-06-16T22:54:03+0000   
Location:                       mil01   
Master URL:                     https://c5.par01.containers.cloud.ibm.com:27949   
Public Service Endpoint URL:    https://c5.par01.containers.cloud.ibm.com:27949   
Private Service Endpoint URL:   -   
Master Location:                par01   
Master Status:                  Ready (4 days ago)   
Master State:                   deployed   
Master Health:                  normal   
Ingress Subdomain:              - †   
Ingress Secret:                 - †   
Ingress Status:                 -   
Ingress Message:                -   
Workers:                        1   
Worker Zones:                   mil01   
Version:                        1.17.7_1529   
Creator:                        -   
Monitoring Dashboard:           -   
Resource Group ID:              6b868616992543618f6e1774d4249fc4   
Resource Group Name:            Default   
† Your Ingress subdomain and secret might not be ready yet. For more info by cluster type, see 'https://ibm.biz/ingress-sub' for Kubernetes or 'https://ibm.biz/ingress-sub-ocp' for OpenShift.
```

## ibmcloud ks workers -c yiyicluster-free
---> worker id
```
OK
ID                                                       Public IP         Private IP       Flavor   State    Status   Zone    Version   
kube-brkkr2of0je3ktpg9lf0-yiyicluster-default-000000dd   159.122.178.183   10.144.213.119   free     normal   Ready    mil01   1.17.6_1527*   

* To update to 1.17.7_1529 version, run 'ibmcloud ks worker update'. Review and make any required version changes before you update: 'https://ibm.biz/upworker'
```
