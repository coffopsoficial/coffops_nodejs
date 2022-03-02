# Projeto Simples Docker + NodeJS

Esse Projeto contém Arquivos para subir uma aplicação em NodeJS usando docker. É totalmente didático para você dar os primeiros passos no mundo do docker.
## Recomendações

Docker Instalado e Rodando;

VSCode para facilitar a vida;

# Explicação do Dockerfile
```bash
FROM node --> informa de qual imagem será gerada essa imagem atual que estamos fazendo;
WORKDIR /appjs --> informa qual será o diretório de trabalho desse container;
COPY app.js . --> copia o arquivo app.js para nosso diretório de trabalho, appjs;
EXPOSE 3000 --> expõe a porta para acesso a aplicação, a mesma que definimos lá no app.js;
CMD ["node", "index.js"] --> é o comando que vai ser executado ao final de todo o processo, subindo nossa aplicação NodeJS;
```

# Comandos

```bash
docker build -t coffops_nodejs:dev-v0.1 .
docker run --name coffops_nodejs_app -p 3000:3000 -d coffops_nodejs:dev-v0.1