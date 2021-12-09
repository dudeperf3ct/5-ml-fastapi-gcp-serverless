### Deploy ML model to GCP using FastAPI

GCP app: https://wine-ratings-b4yojuwgbq-uc.a.run.app/

In this exercise, we will build a fastapi ML application and deploy it with continuous delivery on GCP using Cloud Run and Cloud Build..

### ML

To build a ML model, refer the colab notebook under `notebooks` folder.

### FastAPI

To validate the fastapi application locally,

```bash
docker build -t wine .
docker run --rm -it -v $(pwd):/app -p 8000:8000 wine
```

### GCP

To deploy the fastapi application on GCP following steps were taken.

1. While creating repo, add Google Cloud Build from Marketplace.

2. Create google cloud account.

3. Create a service in `Cloud Run` adding this repo as `Continous Deploy from source repository`

   > Add 8000 under Containers in section Container, Variables & Secrets, Connections, Security

4. App will deployed, to monitor keep checking logs.