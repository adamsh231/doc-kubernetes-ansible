LINUX AMI - CENTOS

1. Create Host File (create pem file from aws, chmod 400)
2. run 1-dep.yaml 
3. run 2-master.yaml -> change flannel
    - export kubever=$(kubectl version | base64 | tr -d '\n')
    - kubectl apply -f "https://cloud.weave.works/k8s/net?k8s-version=$kubever"
4. run 3-workers.yaml
    - aws firewall off or inbound rule, container creating problem
    - masih join manual coba auto

NB: [Warning] beware of Ansible cache


HELM

https://www.ayies.com/cara-install-helm-di-kubernetes-cluster/#:~:text=Helm%20adalah%20sebuah%20tool%20untuk,format%20pemaketan%20resource%2Dresource%20kubernetes.&text=Dengan%20bantuan%20Helm%20kita%20semakin,membangun%20software%20didalam%20cluster%20Kubernetes.

https://www.youtube.com/watch?v=fy8SHvNZGeE&ab_channel=IBMCloud
