kubectl create namespace load-testing

# Installing Jmeter distributed

helm install --name jmeter --namespace load-testing -f jmeter_value.yaml stable/distributed-jmeter

# Updating jmeter distributed

helm upgrade jmeter --namespace load-testing stable/distributed-jmeter --set server.replicaCount=0 --wait


# Install influx db
helm repo add bitnami https://charts.bitnami.com/bitnami
helm install --name influx --namespace load-testing bitnami/influxdb

