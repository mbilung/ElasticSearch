# ElasticSearch
This repository contains the manifest files to deploy a Single node elasticsearch cluster on AKS.
<p>
  
1. kubectl apply -f ES-StorageClass.yml</br>
<i>Creates a storage class with reclaimPolicy: Retain, so that your pods don't lose data once they shutdown/die.</i>
    
2. kubectl apply -f ES-PersistentVolumeClaim.yml</br>
<i>Creates a persistent volume claim to the storage class.</i>

3. kubectl apply -f ES-Deployment.yml</br>
<i>Deploys single node elasticsearch cluster on AKS.</i>

4. kubectl apply -f ES-Service.yml</br>
<i>Exposes elasticsearch single node cluster through port 9200.</i>
</p>
How to access elasticsearch from your local:</br>
>kubectl port-forward service/elasticsearch 8080:9200
