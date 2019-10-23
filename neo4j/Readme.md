helm install --name neo4j-helm stable/neo4j --set acceptLicenseAgreement=yes --set neo4jPassword=

helm install --name neo4j --namespace neo4j stable/neo4j --set neo4jPassword=

