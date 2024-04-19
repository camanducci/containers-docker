# Passo 1: Estrutura do Projeto

Primeiro, vamos criar uma estrutura básica para o projeto Python Vamos supor que temos um diretório com os seguintes arquivos:

 ```
app/
  |- app.py
  |- Dockerfile
```
- app.py: O código-fonte da nossa aplicação Python.
- Dockerfile: O arquivo usado para construir a imagem Docker.

# Passo 2: Dockerfile

Dentro do diretório app, vamos criar o Dockerfile.

# Passo 3: Construir e Testar a Imagem Localmente

Construa a imagem Docker localmente usando o Dockerfile que criamos:

```
docker build -t meu-app-flask .
```

Em seguida, execute um contêiner localmente para testar nossa aplicação:

```
docker run -p 8080:8080 meu-app-flask
```

# Passo 4: Fazer Login no Docker Hub

Se você ainda não tiver uma conta no Docker Hub, crie uma em hub.docker.com. Em seguida, faça login na linha de comando usando o seguinte comando e siga as instruções:

```
docker login
```

# Passo 5: Enviar a Imagem para o Docker Hub

Agora, vamos enviar nossa imagem para o Docker Hub. Primeiro, renomeie a imagem para incluir seu nome de usuário no Docker Hub:

```
docker tag meu-app-flask seu_nome_de_usuario/meu-app-flask
```

Em seguida, faça o push da imagem para o Docker Hub:

```
docker push seu_nome_de_usuario/meu-app-flask
```



