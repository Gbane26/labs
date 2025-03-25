kubectl apply -f influxdb.yml 

kubectl apply -f grafana.yml 

kubectl get pods -o wide  # Pour voir l'adresse IP

kubectl apply -f meteo.yml 

kubectl delete pod influxdb-pod   #Suprimer

kubectl apply -f influxdb-service.yml
kubectl apply -f grafana-service.yml

kubectl get service
kubectl describe service influxdb-service
kubectl describe service grafana-service

minikube service grafana-service

minikube ip

kubectl apply -f grafana-ingress.yml
kubectl apply -f influxdb-ingress.yml

http://monitoring.192.168.49.2.nip.io

http://influxdb.192.168.49.2.nip.io