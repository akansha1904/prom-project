# prom-project
# prometheus-grafana setup
# build python app
docker-compose -f docker-compose.yml up -d
docker push gcr.io/tomcat-70998/prom-project:v1
gcloud auth activate-service-account --key-file=${CREDENTIALS_ID}
gcloud container clusters get-credentials tomcat-service --zone us-central1-c --project tomcat-70998
kubectl create -f deployment.yaml -f service.yml
kubectl get svc
external-ip:8371
# prometheus-grafana setup
docker-compose -f docker-compose.yml up -d


