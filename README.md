# Technical
Step 1. ACtive kubernetes in docker desktop.
step 2. installed the kubernetes dashboard useing this command
kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.0.0/aio/deploy/recommended.yaml
step 3 used the yaml file for jenkins to make that it is persistent since everytime docker closed it would reset jenkins.
step 4 got the admin password from the logs using this command kubectl logs jenkins-6fb994cfc5-twnvn -n jenkins
step 5 created a jenkins workspace and also a jenkins agent that will be running when the jenkins job kicks off
step 6 created a ubuntu node that will have the credentials of the jenkins-agent i have made in ubuntu.
step 7 made a jenkins freeflowing project and choose github as source so it would pull from the rebo that i made where the yaml files will be when deploying to kubernetes. URL for github for deployment :https://github.com/Elementalist371/eShopOnWeb.git
step 8 I used kompose on the github repo for the repo i had to deploy on kubernetes. I used kompose on the docker file for it to generate the service and deployment yaml files needed.
step 9 Configured the yaml files made so that it would run on custom ports.
step 10 run jenkins to deploy to kubernetes 
