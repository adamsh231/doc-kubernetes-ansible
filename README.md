LINUX AMI - CENTOS

1. Create Host File (create pem file from aws, chmod 400)
2. run 1-dep.yaml 
3. run 2-master.yaml -> change flannel
    - export kubever=$(kubectl version | base64 | tr -d '\n')
    - kubectl apply -f "https://cloud.weave.works/k8s/net?k8s-version=$kubever"
        or
    - kubectl apply -f "https://cloud.weave.works/k8s/net?k8s-version=$(kubectl version | base64 | tr -d '\n')"
    nb: Before installing Weave Net, you should make sure the following ports are not blocked by your firewall: TCP 6783 and UDP 6783/6784.
4. run 3-workers.yaml
    - aws firewall off or inbound rule, container creating problem
    - masih join manual coba auto

NB: [Warning] beware of Ansible cache

--------------------------------------------------- Security Group AWS -----------------------------------------------------------
https://www.cloudiqtech.com/creating-aws-security-groups-for-kubernetes/

https://stackoverflow.com/questions/62110917/pods-are-remain-containercreating-networkplugin-cni-failed-to-set-up-pod-netplu (6783 and 6784 for weave network)

https://www.weave.works/docs/net/latest/kubernetes/kube-addon/


---------------------------------------------------  HELM  ------------------------------------------------------------------------

https://www.youtube.com/watch?v=fy8SHvNZGeE&ab_channel=IBMCloud

https://www.youtube.com/watch?v=-ykwb1d0DXU&ab_channel=TechWorldwithNana

https://www.baeldung.com/kubernetes-helm

Helm issue - https://github.com/fnproject/fn-helm/issues/21
