🐛 Troubleshooting
#Check Pod status
kubectl get pods

.If a Pod is not running:

kubectl describe pod <pod-name>
Check Pod logs

#MongoDB:

kubectl logs deployment/mongodb

Mongo Express:

kubectl logs deployment/mongo-express
Check Services
kubectl get svc
Check Service endpoints
kubectl get endpoints

.If MongoDB Service has no endpoint, verify that the Service selector matches the MongoDB Pod labels.

Check MongoDB Service DNS

Mongo Express should use:

mongodb-service

and not:

localhost

Inside Kubernetes, localhost refers to the same Pod/container, not another Pod.
