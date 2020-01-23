# flask_app

### Construir imagem 

```sh
docker build -t flask_app .
```

### Executar imagem 

```sh
docker run --rm -d -p 8000:80 -v $(pwd):/main:z --name my_docker_flask flask_app
```

### Entrar na imagem 

```sh
docker exec -it my_docker_flask bash
```

### Comando para treinamento (requisição GET)

URL_APP:8000/train

### Comando para predição (requisição POST)

curl -i -X POST -H 'Content-Type: application/json' -d '[  {"Age": 85, "Sex": "male", "Embarked": "S"}, {"Age": 24, "Sex": "female", "Embarked": "C"},{"Age": 3, "Sex": "male", "Embarked": "C"}, {"Age": 21, "Sex": "male", "Embarked": "S"}]' URL_APP:8000/predict

### Projeto baseado em:

Flask API for training and predicting using scikit learn models. Link: https://github.com/amirziai/sklearnflask/
