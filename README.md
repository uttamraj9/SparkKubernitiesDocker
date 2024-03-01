Link to my docker image in Dockerhub:
https://hub.docker.com/r/uttamraj9/pysparkkube01

Step 1: Create docker image and create docker image and run locally
cd to dpyspark folder
>cd dpyspark
>docker build -t kubepyspark .
>docker run kubepyspark
--Tag the docker image
>docker tag pysparkkube01 uttamraj9/pysparkkube01:pysparkkube
--push docker image to docker hub
>docker push uttamraj9/pysparkkube01:pysparkkube
--deploye docker image in kubernities
>kubectl apply -f deployment.yaml
Check the status of the Job:
>kubectl get jobs
View detailed information about the Job:
>kubectl describe job my-job-new
Check the status of the pods created by the Job:
>kubectl get pods
View logs of the pods:
>kubectl logs <pod-name>
Monitor the progress of the Job:
>kubectl logs -f <pod-name>   # To continuously stream logs
