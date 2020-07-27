## kubectl get pods

## kubectl get pods -o wide
```
NAME                                  READY   STATUS             RESTARTS   AGE     IP               NODE             NOMINATED NODE   READINESS GATES
hello-97ddc5576-655q6                 1/1     Running            0          5d22h   172.30.254.242   10.144.213.119   <none>           <none>
hello-97ddc5576-ctf7h                 1/1     Running            0          5d22h   172.30.254.244   10.144.213.119   <none>           <none>
hello-97ddc5576-kvjzl                 1/1     Running            0          5d22h   172.30.254.243   10.144.213.119   <none>           <none>
hw-demo-deployment-6c965d5dcd-6nrk8   0/1     CrashLoopBackOff   2455       5d22h   172.30.254.247   10.144.213.119   <none>           <none>
hw-demo-deployment-6c965d5dcd-blv5n   0/1     CrashLoopBackOff   2449       5d22h   172.30.254.246   10.144.213.119   <none>           <none>
hw-demo-deployment-6c965d5dcd-qcdzk   0/1     CrashLoopBackOff   2451       5d22h   172.30.254.245   10.144.213.119   <none>           <none>
watson-pod-57ccbb6cd8-nksrl           1/1     Running            0          5d17h   172.30.254.214   10.144.213.119   <none>           <none>
watson-talk-pod-569c554fc6-n6hbp      1/1     Running            0          5d17h   172.30.254.209   10.144.213.119   <none>           <none>
```

## kubectl get podsa --show-labels
```
NAME                           READY   STATUS    RESTARTS   AGE   LABELS
hello-world-7786fcfc5f-67s26   1/1     Running   0          46h   pod-template-hash=7786fcfc5f,run=hello-world
hello-world-7786fcfc5f-7gkvg   1/1     Running   0          46h   pod-template-hash=7786fcfc5f,run=hello-world
hello-world-7786fcfc5f-kg4bb   1/1     Running   0          46h   pod-template-hash=7786fcfc5f,run=hello-world
hello-world-7786fcfc5f-krv9g   1/1     Running   0          46h   pod-template-hash=7786fcfc5f,run=hello-world
hello-world-7786fcfc5f-lpjxt   1/1     Running   0          46h   pod-template-hash=7786fcfc5f,run=hello-world
hello-world-7786fcfc5f-r6l2s   1/1     Running   0          46h   pod-template-hash=7786fcfc5f,run=hello-world
hello-world-7786fcfc5f-vcskv   1/1     Running   0          46h   pod-template-hash=7786fcfc5f,run=hello-world
```

## kubectl get pod hello-97ddc5576-655q6 -o yaml
```
apiVersion: v1
kind: Pod
metadata:
  annotations:
    kubernetes.io/psp: ibm-privileged-psp
  creationTimestamp: "2020-06-18T17:28:52Z"
  generateName: hello-97ddc5576-
  labels:
    pod-template-hash: 97ddc5576
    run: hello
  name: hello-97ddc5576-655q6
  namespace: default
  ownerReferences:
  - apiVersion: apps/v1
    blockOwnerDeletion: true
    controller: true
    kind: ReplicaSet
    name: hello-97ddc5576
    uid: 6847439b-0bca-4bbf-b3ae-4803e46fd7bd
  resourceVersion: "220729"
  selfLink: /api/v1/namespaces/default/pods/hello-97ddc5576-655q6
  uid: 5e882719-5436-4148-b4b8-32c234a4ad38
spec:
  containers:
  - image: us.icr.io/yiyitest1/hello-world:1
    imagePullPolicy: IfNotPresent
    name: hello
    resources: {}
    terminationMessagePath: /dev/termination-log
    terminationMessagePolicy: File
    volumeMounts:
    - mountPath: /var/run/secrets/kubernetes.io/serviceaccount
      name: default-token-lrbvt
      readOnly: true
  dnsPolicy: ClusterFirst
  enableServiceLinks: true
  imagePullSecrets:
  - name: default-icr-io
  - name: default-us-icr-io
  - name: default-uk-icr-io
  - name: default-de-icr-io
  - name: default-au-icr-io
  - name: default-jp-icr-io
  - name: all-icr-io
  nodeName: 10.144.213.119
  priority: 0
  restartPolicy: Always
  schedulerName: default-scheduler
  securityContext: {}
  serviceAccount: default
  serviceAccountName: default
  terminationGracePeriodSeconds: 30
  tolerations:
  - effect: NoExecute
    key: node.kubernetes.io/not-ready
    operator: Exists
    tolerationSeconds: 600
  - effect: NoExecute
    key: node.kubernetes.io/unreachable
    operator: Exists
    tolerationSeconds: 600
  volumes:
  - name: default-token-lrbvt
    secret:
      defaultMode: 420
      secretName: default-token-lrbvt
status:
  conditions:
  - lastProbeTime: null
    lastTransitionTime: "2020-06-18T17:28:52Z"
    status: "True"
    type: Initialized
  - lastProbeTime: null
    lastTransitionTime: "2020-06-18T17:28:54Z"
    status: "True"
    type: Ready
  - lastProbeTime: null
    lastTransitionTime: "2020-06-18T17:28:54Z"
    status: "True"
    type: ContainersReady
  - lastProbeTime: null
    lastTransitionTime: "2020-06-18T17:28:52Z"
    status: "True"
    type: PodScheduled
  containerStatuses:
  - containerID: containerd://a1cebf39ee7f56499dfa766b2746a15148da580fb4295b4057dc2f56e2a0afe3
    image: us.icr.io/yiyitest1/hello-world:1
    imageID: us.icr.io/yiyitest1/hello-world@sha256:de2d7cdc2e877d4578a6a154ebf9b571eaaf5aca8174181d53da57e373c60257
    lastState: {}
    name: hello
    ready: true
    restartCount: 0
    started: true
    state:
      running:
        startedAt: "2020-06-18T17:28:54Z"
  hostIP: 10.144.213.119
  phase: Running
  podIP: 172.30.254.242
  podIPs:
  - ip: 172.30.254.242
  qosClass: BestEffort
  startTime: "2020-06-18T17:28:52Z"
```
## kubectl get pods --all-namespaces
## kubectl get pod --all-namespaces| grep -i vpn
```
NAMESPACE     NAME                                           READY   STATUS             RESTARTS   AGE
default       hello-97ddc5576-655q6                          1/1     Running            0          8d
default       hello-97ddc5576-ctf7h                          1/1     Running            0          8d
default       hello-97ddc5576-kvjzl                          1/1     Running            0          8d
default       hw-demo-deployment-6c965d5dcd-6nrk8            0/1     CrashLoopBackOff   3377       8d
default       hw-demo-deployment-6c965d5dcd-blv5n            1/1     Running            3372       8d
default       hw-demo-deployment-6c965d5dcd-qcdzk            0/1     CrashLoopBackOff   3374       8d
default       watson-pod-57ccbb6cd8-nksrl                    1/1     Running            0          7d23h
default       watson-talk-pod-569c554fc6-n6hbp               1/1     Running            0          7d23h
ibm-system    addon-catalog-source-j8hrl                     1/1     Running            0          3d5h
ibm-system    catalog-operator-5fdf997564-cj6fm              1/1     Running            0          9d
ibm-system    olm-operator-5bf86499cc-tqjnq                  1/1     Running            0          9d
kube-system   calico-kube-controllers-5754cfb59d-w85x5       1/1     Running            0          32h
kube-system   calico-node-9pmhc                              1/1     Running            0          32h
kube-system   coredns-6567db4fff-fp8xm                       1/1     Running            0          9d
kube-system   coredns-6567db4fff-q244f                       1/1     Running            0          9d
kube-system   coredns-6567db4fff-z9zbl                       1/1     Running            0          9d
kube-system   coredns-autoscaler-649976fbf4-gt9h8            1/1     Running            0          9d
kube-system   dashboard-metrics-scraper-5789d44f58-8qj6d     1/1     Running            0          9d
kube-system   ibm-keepalived-watcher-tskgt                   1/1     Running            0          9d
kube-system   ibm-master-proxy-static-10.144.213.119         2/2     Running            0          9d
kube-system   kubernetes-dashboard-6cfcf747-wtj54            1/1     Running            0          32h
kube-system   metrics-server-857d7b5b77-k7m7k                2/2     Running            0          32h
kube-system   vpn-f66c45467-rmrf6                            1/1     Running            0          9d
razeedeploy   remoteresource-controller-589f6886fc-b8sq9     1/1     Running            0          4d
```

## kubectl describe pod hello-world-7bd7f9c949-9dx54
```
Name:         hello-world-7bd7f9c949-9dx54
Namespace:    default
Priority:     0
Node:         10.144.213.119/10.144.213.119
Start Time:   Wed, 17 Jun 2020 18:30:29 -0700
Labels:       pod-template-hash=7bd7f9c949
              run=hello-world
Annotations:  kubernetes.io/psp: ibm-privileged-psp
Status:       Pending
IP:           172.30.254.227
IPs:
  IP:           172.30.254.227
Controlled By:  ReplicaSet/hello-world-7bd7f9c949
Containers:
  hello-world:
    Container ID:   
    Image:          us.icr.io/yiyitest1/hello-world
    Image ID:       
    Port:           <none>
    Host Port:      <none>
    State:          Waiting
      Reason:       ImagePullBackOff
    Ready:          False
    Restart Count:  0
    Environment:    <none>
    Mounts:
      /var/run/secrets/kubernetes.io/serviceaccount from default-token-lrbvt (ro)
Conditions:
  Type              Status
  Initialized       True 
  Ready             False 
  ContainersReady   False 
  PodScheduled      True 
Volumes:
  default-token-lrbvt:
    Type:        Secret (a volume populated by a Secret)
    SecretName:  default-token-lrbvt
    Optional:    false
QoS Class:       BestEffort
Node-Selectors:  <none>
Tolerations:     node.kubernetes.io/not-ready:NoExecute for 600s
                 node.kubernetes.io/unreachable:NoExecute for 600s
Events:
  Type     Reason   Age                     From                     Message
  ----     ------   ----                    ----                     -------
  Normal   BackOff  43m (x3728 over 14h)    kubelet, 10.144.213.119  Back-off pulling image "us.icr.io/yiyitest1/hello-world"
  Warning  Failed   3m58s (x3902 over 14h)  kubelet, 10.144.213.119  Error: ImagePullBackOff

kubectl describe deployment
Name:                   hello-world
Namespace:              default
CreationTimestamp:      Wed, 17 Jun 2020 17:31:48 -0700
Labels:                 run=hello-world
Annotations:            deployment.kubernetes.io/revision: 2
Selector:               run=hello-world
Replicas:               10 desired | 7 updated | 13 total | 0 available | 13 unavailable
StrategyType:           RollingUpdate
MinReadySeconds:        0
RollingUpdateStrategy:  25% max unavailable, 25% max surge
Pod Template:
  Labels:       run=hello-world
  Annotations:  kubectl.kubernetes.io/restartedAt: 2020-06-17T18:18:27-07:00
  Containers:
   hello-world:
    Image:        us.icr.io/yiyitest1/hello-world
    Port:         <none>
    Host Port:    <none>
    Environment:  <none>
    Mounts:       <none>
  Volumes:        <none>
Conditions:
  Type           Status  Reason
  ----           ------  ------
  Available      False   MinimumReplicasUnavailable
  Progressing    False   ProgressDeadlineExceeded
OldReplicaSets:  hello-world-7bd7f9c949 (6/6 replicas created)
NewReplicaSet:   hello-world-f694c5c9f (7/7 replicas created)
Events:          <none>
Yiyis-MacBook-Pro:~ yiyi.zhou@ibm.com$ kubectl rollout status deployment/hello-world
^[[D^[[D^[[D^[[Derror: deployment "hello-world" exceeded its progress deadline
Yiyis-MacBook-Pro:~ yiyi.zhou@ibm.com$ kubectl rollout restart deployment/hello-world
deployment.apps/hello-world restarted
```


## kubectl get replicasets
```
NAME                            DESIRED   CURRENT   READY   AGE
hello-97ddc5576                 3         3         3       5d23h
hello-bf9597fdf                 0         0         0       5d23h
hw-demo-deployment-6c965d5dcd   3         3         2       5d22h
watson-pod-57ccbb6cd8           1         1         1       5d17h
watson-talk-pod-569c554fc6      1         1         1       5d17h
```
## kubectl delete deployment <NAME>
Then all corresponded pods of <name> will terminate by itself. Otherwise deleting specific pods will only result into creating new pods.
