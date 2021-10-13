# ElasticSearch
This repository contains the manifest files to deploy a Single node elasticsearch cluster on AKS.
<p>
What does each file do?

1. ES-StorageClass.yml: Creates a storage class with reclaimPolicy: Retain, so that your pods don't lose data once they shutdown
2. ES-PersistentVolumeClaim.yml: Creates a volume claim to the storage class
3. ES-Deployment.yml: Deploys single node elasticsearch cluster on AKS
4. ES-Service.yml: Exposes elasticsearch single node cluster through port 9200
</p>

How to access elasticsearch from your local:</br>
>kubectl port-forward service/elasticsearch 8080:9200
