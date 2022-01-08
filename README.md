# EFK

>We’ll be using ElasticSearch (Storage), Fluentd (Logging Layer), and Kibana (Visualization) to store, aggregate & visualise logs.

## Requirements

- kubectl (check via kubectl version)
- a working kube-context with access to a Kubernetes cluster (check with kubectl get namespaces)

## Steps

reference: [EFK guide](https://medium.com/@chris_linguine/how-to-monitor-distributed-logs-in-kubernetes-with-the-efk-stack-1218a565ce0c)

- get file EFK

```
git clone https://github.com/darkmtrance/EFK.git
cd EFK
```

![git clone](Images/Screenshot_0.png)

- install EFK

```
kubectl apply -f .
```

![kubectl apply](Images/Screenshot_1.png)

- access to kibana 

```
kubectl get svc -n efklog
```

![kubectl get](Images/Screenshot_2.png)

- open the service kibana-logging http://52.151.229.136:5601 in your browser

![kibana init](Images/Screenshot_3.png)

>You now have Kibana

- Once it has loaded, click on the management icon, and go to index patterns

![kibana 2](Images/Screenshot_4.png)

- Click Create index pattern

![kibana 3](Images/Screenshot_5.png)

- Enter ```logstash-*``` in the field for the index pattern

![kibana 4](Images/Screenshot_6.png)

- Click Next step & Select @ timestamp & Create index pattern

![kibana 5](Images/Screenshot_7.png)

- You should now have a valid index pattern

![kibana 6](Images/Screenshot_8.png)

- You should now be able to see all your logs in Kibana. On the Kibana dashboard, go to the Discover page.

![kibana 7](Images/Screenshot_9.png)
