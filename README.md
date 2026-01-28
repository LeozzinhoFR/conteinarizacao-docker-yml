# 🐳 Desafio de Conteinerização com Docker

Este repositório contém o conteúdo de uma conteinerização simples. O objetivo do repositório foi criar uma estrutura de microsserviços utilizando **Docker** e **Docker Compose** para hospedar uma página web estática com servidor Apache.

## 🖥️ Resultado Visual

Abaixo está o resultado da página renderizada no navegador, rodando dentro do container:

![Resultado do Projeto](https://github.com/LeozzinhoFR/conteinarizacao-docker-yml/blob/main/funcionando.png)

> "RONCOLATO fez o dever de casa" - Página estilizada com tema Terminal/Matrix.

## 🛠️ Tecnologias Utilizadas

* **Docker**: Para criação e gerenciamento do container.
* **Docker Compose**: Para orquestração do serviço e definição de infraestrutura como código.
* **Apache HTTP Server (httpd)**: Imagem oficial utilizada como servidor web.
* **HTML5 & CSS3**: Para a criação da interface estilo "Hacker/Neon".

## 📂 Estrutura do Projeto

A estrutura de arquivos do projeto está organizada da seguinte maneira:

```text
.
├── docker-compose.yml    # Arquivo de orquestração do container
├── website/              # Diretório mapeado para o container (Volume)
│   └── index.html        # Página principal com o estilo terminal
└── image_04e57d.png      # Screenshot do projeto

```

## ⚙️ Configurações do Docker Compose

O arquivo `docker-compose.yml` foi configurado com as seguintes especificações:

* **Versão**: 3.9
* **Serviço (`apache`)**:
* Imagem: `httpd:latest`
* Nome do Container: `my-apache-app`
* **Portas**: Mapeamento da porta `80` do host para a porta `80` do container.
* **Volumes**: Bind Mount da pasta `./website` local para `/usr/local/apache2/htdocs` no container. Isso permite editar o HTML localmente e ver as alterações em tempo real.


* **Rede**: Criação de uma bridge network chamada `projeto1-dio`.

## 🚀 Como Executar

Pré-requisitos: Tenha o [Docker](https://www.docker.com/) e o [Docker Compose](https://docs.docker.com/compose/) instalados na sua máquina.

1. **Clone o repositório:**
```bash
git clone [https://github.com/leozzinhofr/conteinarizacao-docker-yml.git](https://github.com/leozzinhofr/conteinarizacao-docker-yml.git)
cd conteinarizacao-docker-yml

```


2. **Suba o container:**
No terminal, dentro da pasta do projeto, execute:
```bash
docker-compose up -d

```


3. **Acesse a página:**
Abra o seu navegador e acesse:
* [http://localhost:80](https://www.google.com/search?q=http://localhost:80)
* Ou utilize o IP da sua máquina (ex: `192.168.x.x`) se estiver acessando de outro dispositivo na rede.


4. **Parar a execução:**
Para parar e remover os containers criados:
```bash
docker-compose down
```



---

Desenvolvido por **Leonardo Roncolato**.
