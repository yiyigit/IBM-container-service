
- http://localhost:8001/api/v1/namespaces
- http://localhost:8001/api/v1/namespaces/default/pods
## kubectl get endpoints
```
NAME                  ENDPOINTS                                                     AGE
hello-second          172.30.254.242:8080,172.30.254.243:8080,172.30.254.244:8080   11d
kubernetes            172.20.0.1:2040                                               4d8h
watson-service        172.30.254.214:8081                                           10d
watson-talk-service   172.30.254.209:8080                                           10d
```
## kubectl cluster-info 
Display addresses of the master and services to retrieve the service's proxy URL

```
Kubernetes master is running at https://c5.par01.containers.cloud.ibm.com:27949
CoreDNS is running at https://c5.par01.containers.cloud.ibm.com:27949/api/v1/namespaces/kube-system/services/kube-dns:dns/proxy
kubernetes-dashboard is running at https://c5.par01.containers.cloud.ibm.com:27949/api/v1/namespaces/kube-system/services/https:kubernetes-dashboard:/proxy
Metrics-server is running at https://c5.par01.containers.cloud.ibm.com:27949/api/v1/namespaces/kube-system/services/https:metrics-server:/proxy
NodeLocalDNS is running at https://c5.par01.containers.cloud.ibm.com:27949/api/v1/namespaces/kube-system/services/node-local-dns:dns/proxy

```
