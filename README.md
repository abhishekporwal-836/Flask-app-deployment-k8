## Description
### Implementation PDF: Open the file "Implementaion_PDF"
DockerHub Repo Link : [Click here!](https://hub.docker.com/repository/docker/abhishekporwal836/flask-app-buyogo/general)

# Report:

1. **Python Flask Application:**
   - Endpoints are working fine as shown in the implementation pdf and all the steps are mentioned on Page 1
   - Ensured that the application is deployed with 2 replicas which can be verified from the manifests -> flask-deployment.yaml and also in the pdf on Page  number 4.

2. **Database:**
   - Ensured that the MongoDB uses authentication to secure data access and also updated the code to use authentication to connect with mongoDB , this can be verified through manifests mongo-secret.yaml , app.env and app.python

3. **Kubernetes Setup:**
   - Used Minikube setup for the orchestration implementation and the steps are shown in implementation pdf Page no 2.

4. **Pod Deployment:** Can be seen on Page 3 of pdf
   - Flask Application Deployment: Created deployment for the Flask application with least 2 replicas through flask-deployment.yaml.
   - MongoDB StatefulSet: Created StatefulSet for MongoDB with authentication enabled using mongo-deployment.yaml and mongo-secret.yaml .

5. **Services:** Can be seen on Page 3&4
   - Created  Service to expose the Flask application using flask-service.yaml and accessed it through port forwarding.
   - Create a Service to allow the Flask application to connect to MongoDB, using mongo-service.yaml.

6. **Volumes:**
   - Didn't implemented. 

7. **Autoscaling:**
   - The Horizontal Pod Autoscaler (HPA) scales the Flask application pods based on CPU usage, with a threshold of 70% utilization. It maintains a minimum of 2 replicas and scales up to a maximum of 5 replicas, as specified in flask-autoscaler.yaml.
   - Page 5 in pdf for reference.
8. **DNS Resolution:**
   - Kubernetes uses a built-in DNS system to help pods find and talk to each other by using service names instead of IP addresses. This makes it easier for different parts of your application to communicate within the cluster.
   - I tried implementing it but got stuck with some error which is shown on Page 5 in pdf for reference.
9.  **Resource Management**
   - Configured resource requests and limits for both the Flask and MongoDB pods and have marked the changes in flask-deployment.yaml and mongo-deployment.yaml and then run kubectl to apply the manifests.
   - Page 5&6 in pdf for reference.
