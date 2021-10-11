

1. Criar Dockerfile e dockerignore

2. criar a Docker image (opcionalmente register no Docker Registry -> version + latest):
```bash
cd src/

docker image build -t nunojacinto/conversao-temperatura:v1 .
```

3. Executar container localmente
```bash
docker container run -p 8080:8080 --name temperatura -d  nunojacinto/conversao-temperatura:v1
```

4. Confirm status
```bash
docker container ls -a
```
& visit http://localhost:8080/