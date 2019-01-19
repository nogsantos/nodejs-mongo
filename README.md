# NodeJS - Express - Marko and Moongose

[Marko serve side render](https://markojs.com/)


## Setup

### Conteiner build

No projeto há um arquivo para criar o container, com o comando abaixo, será realizado o build para gerar a imagem.

```bash
$ docker build -f node.dockerfile -t local/node-mongo .
```
> Flags:
> - `-f` Nome do arquivo dockerfile que será utilizado para realizar o build da imagem
> - `-t` Nome da imagem

### Subir conteiner

Após realizado o build do container, para subí-lo

```bash
$ docker run -d --name nodejs -p 8080:3000 --network nogsantos local/node-mongo
```
> Flags:
> - `-d` Executar contêiner em background
> - `--name` Dá um nome ao container
> - `-p` Associa uma porta do host à porta exposta no container
> - `--network` Associa uma rede ao container
