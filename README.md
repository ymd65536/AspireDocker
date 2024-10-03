# AspireDocker

```bash
docker build -t aspire . --platform=linux/amd64
```

```bash
docker run --name test -p 18888:18888 -e DOTNET_DASHBOARD_UNSECURED_ALLOW_ANONYMOUS="true" aspire
```

```bash
docker rm test
```

## Artifact Registryのセットアップ

```bash
export PROJECT_ID=`gcloud config get-value project`
gcloud auth login
gcloud auth configure-docker asia-northeast1-docker.pkg.dev
docker tag aspire asia-northeast1-docker.pkg.dev/$PROJECT_ID/aspire/aspire:latest
docker push asia-northeast1-docker.pkg.dev/$PROJECT_ID/aspire/aspire:latest
```

```bash

## AWS CLIのセットアップ

```bash
curl 'https://awscli.amazonaws.com/awscli-exe-linux-'$(uname -m)'.zip' -o 'aws-cli.zip' && \
    unzip aws-cli.zip && \
    sudo ./aws/install && \
    rm -rf aws aws-cli.zip
```
