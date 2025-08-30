Kubernetes-service-
This YAML file creates a Kubernetes Service named souravservice.
It exposes your application (souravapp) to the outside world using a LoadBalancer.

apiVersion: v1 → Version of Kubernetes API used.

kind: Service → Tells Kubernetes that this is a Service resource.

metadata.name: souravservice → The name of the Service.

spec.ports →

port: 3456 → Exposed port for external users.

targetPort: 80 → The port inside the pod where the app is running.

selector.app: souravapp → Selects pods with the label app: souravapp.

type: LoadBalancer → Makes the service accessible from outside the cluster (via cloud load balancer).


Run the following command:

kubectl apply -f souravservice.yaml

Check Service
kubectl get services
