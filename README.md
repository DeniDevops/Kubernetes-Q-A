# Kubernetes-Q-A
Kubernetes is an open-source container orchestration platform that automates deployment, scaling, and management of containerized applications. 
 
50 Best Interview Questions and Answers on Kubernetes
Basic Kubernetes Questions
1.	What is Kubernetes?
Kubernetes is an open-source container orchestration system for automating application deployment, scaling, and management.
2.	What are the main components of Kubernetes?
o	Master Node: API Server, Controller Manager, Scheduler, etcd
o	Worker Node: Kubelet, Kube Proxy, Container Runtime
3.	What is a Pod in Kubernetes?
A Pod is the smallest deployable unit in Kubernetes, encapsulating one or more containers with shared storage and networking.
4.	What is the difference between a Deployment and a StatefulSet?
o	Deployment: Manages stateless applications.
o	StatefulSet: Manages stateful applications with stable network identities and persistent storage.
5.	What is a Service in Kubernetes?
A Service provides a stable network endpoint to expose Pods, enabling load balancing and inter-Pod communication.
Kubernetes Architecture & Components
6.	What is etcd in Kubernetes?
etcd is a distributed key-value store used to maintain cluster state and configuration.
7.	What is the role of the API Server?
The API Server acts as the frontend for Kubernetes, handling REST requests and communicating with etcd.
8.	What is the Kubelet?
The Kubelet is an agent running on worker nodes, ensuring that containers are running as defined in Pod specifications.
9.	What is Kube Proxy?
Kube Proxy maintains network rules on worker nodes to enable service discovery and routing.
10.	How does the Kubernetes Scheduler work?
The Scheduler assigns Pods to worker nodes based on resource availability and constraints.
Networking & Security
11.	How does Kubernetes networking work?
Kubernetes provides a flat network where all Pods can communicate directly without NAT.
12.	What is a Network Policy in Kubernetes?
A Network Policy controls inbound and outbound traffic between Pods.
13.	What are the different types of Kubernetes Services?
o	ClusterIP (default, internal access)
o	NodePort (exposes service on a static port on each node)
o	LoadBalancer (integrates with cloud provider's LB)
o	ExternalName (maps service to an external DNS name)
14.	What is Ingress in Kubernetes?
Ingress manages external access to Services, typically via HTTP/HTTPS.
15.	How do you secure Kubernetes clusters?
o	RBAC (Role-Based Access Control)
o	Network Policies
o	TLS encryption for API communication
o	Pod Security Policies
Storage & Persistence
16.	What is Persistent Volume (PV) in Kubernetes?
A PV is a storage resource in the cluster, provisioned independently of Pods.
17.	What is a Persistent Volume Claim (PVC)?
A PVC is a request for storage by a Pod, dynamically binding to a PV.
18.	What are StorageClasses in Kubernetes?
StorageClasses define storage types and provisioning policies.
19.	What is the difference between emptyDir and hostPath?
o	emptyDir: Temporary storage tied to the Pod's lifecycle.
o	hostPath: Mounts a node's filesystem inside the container.
20.	How do you back up and restore Kubernetes volumes?
Use volume snapshots, cloud storage snapshots, or tools like Velero.
Scaling & Load Balancing
21.	How do you scale applications in Kubernetes?
Use kubectl scale or Horizontal Pod Autoscaler (HPA).
22.	What is Horizontal Pod Autoscaler (HPA)?
HPA automatically adjusts the number of Pods based on CPU/memory usage.
23.	What is Vertical Pod Autoscaler (VPA)?
VPA adjusts resource requests and limits for Pods.
24.	What is Cluster Autoscaler?
Cluster Autoscaler adds or removes nodes based on resource demands.
25.	What is the difference between HPA and VPA?
o	HPA scales the number of Pods.
o	VPA adjusts Pod resource requests.
Deployments & Updates
26.	What are the different types of rolling updates in Kubernetes?
o	RollingUpdate (default, gradually replaces Pods)
o	Recreate (deletes old Pods before creating new ones)
27.	What is a DaemonSet?
A DaemonSet ensures that a specific Pod runs on all (or some) nodes.
28.	What is a Job in Kubernetes?
A Job runs a finite task and ensures successful completion.
29.	What is a CronJob?
A CronJob runs Jobs at scheduled intervals.
30.	How do you perform a rollback in Kubernetes?
Use kubectl rollout undo deployment <deployment-name>.
ConfigMaps & Secrets
31.	What is a ConfigMap?
ConfigMap is used to store non-sensitive configuration data.
32.	What is a Secret in Kubernetes?
A Secret is used to store sensitive data like passwords and API keys.
33.	How do ConfigMaps and Secrets differ?
Secrets are base64-encoded and stored securely, while ConfigMaps store plain-text data.
34.	How do you mount a ConfigMap into a Pod?
o	As environment variables
o	As a volume
35.	How do you mount a Secret into a Pod?
o	As environment variables
o	As a volume
Troubleshooting & Debugging
36.	How do you check Pod logs?
kubectl logs <pod-name>
37.	How do you access a running Pod interactively?
kubectl exec -it <pod-name> -- /bin/sh
38.	How do you check cluster events?
kubectl get events
39.	What command helps debug a failing Pod?
kubectl describe pod <pod-name>
40.	How do you restart a Kubernetes Pod?
Delete the Pod (kubectl delete pod <pod-name>) and let the Deployment recreate it.
Advanced Topics
41.	What is Helm in Kubernetes?
Helm is a package manager for Kubernetes that simplifies application deployment.
42.	What is a Kubernetes Operator?
An Operator extends Kubernetes capabilities by automating application management.
43.	What is Custom Resource Definition (CRD)?
CRDs allow users to define their own Kubernetes resource types.
44.	How does Kubernetes handle high availability?
By running multiple control plane nodes and distributing workloads across worker nodes.
45.	What are taints and tolerations in Kubernetes?
Taints prevent Pods from being scheduled on specific nodes unless they tolerate them.
46.	What is a sidecar container?
A sidecar is a helper container that runs alongside a main application container.
47.	What is service mesh in Kubernetes?
A service mesh (e.g., Istio, Linkerd) manages service-to-service communication with features like traffic management and security.
48.	How do you enforce security policies in Kubernetes?
Using Admission Controllers, Pod Security Standards (PSS), and RBAC.
49.	What are Init Containers?
Init Containers run before the main container to prepare the environment.
50.	How do you monitor a Kubernetes cluster?
Use tools like Prometheus, Grafana, and ELK Stack.

