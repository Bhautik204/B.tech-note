docker ps
minikube start
kubectl get pods -n wareville
kubectl exec -n wareville naughty-or-nice -it -- /bin/bash
cat /var/log/apache2/access.log
exit 
cd /home/ubuntu/dfir_artefacts/
docker ps 
docker exec -it 77fdd ls -al /var/log
docker logs 77fdd
ls
cat docker-registry-logs.log | grep "HEAD" | cut -d ' 'f 1
cat docker-registry-logs.log | grep "10.10.130.253"
cat docker-registry-logs.log | grep "10.10.130.253" | grep "Patch"
cat docker-registry-logs.log | grep "10.10.130.253" | grep "HEAD"
kubectl get rolebindings -n wareville
kubectl describe rolebindings job-runner -n wareville
kubectl describe rolebindings mayor-user -n wareville
kubectl describe role mayor-user -n wareville


