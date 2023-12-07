# Flask Container on Azure App Service

https://learn.microsoft.com/en-us/azure/developer/python/tutorial-containerize-simple-web-app-for-app-service?tabs=web-app-flask

## Startup
### 1. Python Virtual Environment
```bash
python3 -m venv .venv
source .venv/bin/activate 

# WINDOWS
python -m venv .venv
.\.venv\Scripts\activate
```

### 2. Install Requirements
```
pip install -r ./requirements.txt
```

### Run locally
```
flask --app app run
```

## Docker
### Build
```
docker build --tag flask-container-on-azure-app-service .
```

### Run
```
docker run --detach --publish 8080:50505 flask-container-on-azure-app-service
```