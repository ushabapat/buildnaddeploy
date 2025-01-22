# buildnaddeploy

Building of sample .net container based application, which includes build the image using the docker file. Scane the code using sonarqube. I have commented out as I dont have sonar host nad token to feed it. Same case with artifacts. You can use either public or private artifact to push the image.

I have added the trivy task to scan the image. 

The pipeline has automation in place to update the build image tag to the helm chart of the application which is located in the another repo, which in turn deploy the application in AKS using ARGOCD.


# Validate You'll need to add the following secrets to your repository settings:



SONAR_TOKEN: The token for authenticating with SonarQube.
SONAR_HOST_URL: The URL of your SonarQube server.
ARTIFACTORY_USERNAME: Your Artifactory username.
ARTIFACTORY_PASSWORD: Your Artifactory password.
ARTIFACTORY_URL: The URL of your Artifactory registry.
DEPLOYMENT_REPO_TOKEN: A GitHub token with access to the deployment repository.
ARGOCD_SERVER: The URL of your Argo CD server (optional).
ARGOCD_TOKEN: A token for authenticating with Argo CD (optional).
