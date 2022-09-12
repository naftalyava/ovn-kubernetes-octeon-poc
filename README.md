The setup:
 1. k8s control plane node
 2. k8s worker node
 3. dpu node

High level instructions:

1. Build and push ovn-kubernetes for both x86 and aarch64 arch [use build.sh and build_aarch64.sh]
2. Install Kubernetes cluster.
3. Install ovs on k8s control plane node and dpu node.
4. Deploy ovn-kubernetes on k8s cluster using dist/images/deploy.sh script [edit per your setup]
5. Deploy ovn kubernetes on the dpu host using /dist/images/dpu.sh [edit per your parameters]
    5.1 you will need ca.crt, which can be copied from any k8s node. [can be found in /etc/kubernetes/pki folder]

