# ansible-k8s
Vangrantfile and ansible roles to set up a Kubernetes lab locally

# Prerequisites

 - [Vagrant](https://www.vagrantup.com/downloads.html)
 - [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
 - [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
 - [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/) (to interact with the cluster)

## Getting the lab running

 1. After installing the prerequisites you should be able to run and sit back while the cluster is configured.

```
vagrant up
```

 2. Export the **KUBECONFIG** variable pointing to the resulting admin.conf on the root of the proyect.

```bash
export KUBECONFIG=$(pwd)/admin.conf
```

 3. Verify everything is fine by querying the nodes.

```
kubectl get nodes
NAME           STATUS    ROLES     AGE       VERSION
controller-0   Ready     master    1h        v1.10.0
worker-0       Ready     <none>    1h        v1.10.0
worker-1       Ready     <none>    1h        v1.10.0
worker-2       Ready     <none>    1h        v1.10.0
```

Have fun!
