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
   -Used Minikube setup for the orchestration implementation and the steps are shown in implementation pdf Page no 2.
4. **Pod Deployment:** Can be seen on Page 3 of pdf
   - Flask Application Deployment: Created deployment for the Flask application with least 2 replicas through flask-deployment.yaml.
   - MongoDB StatefulSet: Created StatefulSet for MongoDB with authentication enabled using mongo-deployment.yaml and mongo-secret.yaml .
5. **Services:** Can be seen on Page 3&4
   - Created  Service to expose the Flask application using flask-service.yaml and accessed it through port forwarding.
   - Create a Service to allow the Flask application to connect to MongoDB, using mongo-service.yaml.
6. **Volumes:**
7. **Autoscaling:**
8. **DNS Resolution:**
9.  **Resource Management**
