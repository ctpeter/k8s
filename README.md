# Setup
Build image using docker
```
cd app
docker build -t registry.gitlab.com/<repo-name>/<image-name>:<tag> .
```
# Deployment
Manual deployment
```
helm upgrade --install angkas ./angkas \
        --set image.repository=registry.gitlab.com/<repo-name>/<image-name> \
        --set image.tag=<tag> \
        --namespace <namespace> --create-namespace
```
