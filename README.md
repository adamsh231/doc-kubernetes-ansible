1. Create Host File (create pem file from aws, chmod 400)
2. run 1-dep.yaml 
3. run 2-master.yaml -> change flannel
    - export kubever=$(kubectl version | base64 | tr -d '\n')
    - kubectl apply -f "https://cloud.weave.works/k8s/net?k8s-version=$kubever"
4. run 3-workers.yaml
    - aws firewall off or inbound rule
    - masih join manual coba auto
