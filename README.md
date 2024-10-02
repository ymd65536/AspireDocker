# AspireDocker

```bash
docker build -t aspire .
```

```bash
docker run --name test -p 18888:18888 -e DOTNET_DASHBOARD_UNSECURED_ALLOW_ANONYMOUS="true" aspire
```

```bash
docker rm test
```
