# Kubernetes from scratch

## Start up vagrant and connect to master node

    vagrant up
    vagrant ssh master
    sudo su


## 0-PackageInstallation.sh
Notes:
- run package installation on master
- run each command sequentially
- running the shell script as a whole won't work

## 1-CreateMaster.sh

Notes on `kubeadm init`
- creates a self-signed CA
- secures cluster comms (i.e. with API Server)
- authentication of users and kubelets

See: https://kubernetes.io/docs/reference/setup-tools/kubeadm/kubeadm-init/#external-ca-mode

- creates kube .config files (from /etc/kubernetes)
- generates static manifests at /etc/kubernetes/manifests (i.e. for Control Plane)
- creates Pod Networking (using Calico)

Notes: alternatives to Calico are Flannel and Weave Net

- calico.yaml: should already have:

            - name: CALICO_IPV4POOL_CIDR
              value: "192.168.0.0/16"

- after running `sudo kubeadm init --pod-network-cidr=192.168.0.0/16` make note of the `kubeadm join ...` output. E.g. `kubeadm join 10.0.2.15:6443 --token az9vbo.ymf85m7dlj49qu6m     --discovery-token-ca-cert-hash sha256:1b7dc152f29d1ce29110deeeb570eebf73600b615d000250d586e656a6f80c0a`




