# criando_container_Docker
Neste projeto utilizarei o Docker Compose para executar uma aplicação HTML em um Container Apache.

## Passo a Passo: Configurando um Servidor Apache com Docker Compose

Neste tutorial, você aprenderá como configurar um servidor Apache usando o Docker Compose, hospedar uma aplicação web simples e publicar tudo em um repositório no GitHub. Certifique-se de cumprir os pré-requisitos mencionados antes de começar.

### 1. Criar um Arquivo YML com as Definições do Servidor Apache

Crie um arquivo chamado `docker-compose.yml` em um diretório de sua escolha. Abra o arquivo em um editor de texto e adicione o seguinte conteúdo:

```yaml
version: '3'
services:
  webserver:
    image: httpd:latest
    ports:
      - "80:80"
    volumes:
      - ./app:/usr/local/apache2/htdocs/
```

Este arquivo YML define um serviço chamado "webserver" baseado na imagem Docker do servidor Apache. Ele mapeia a porta 80 do contêiner para a porta 80 do host e vincula um volume que conterá os arquivos da aplicação.

### 2. Especificar o Local dos Arquivos da Aplicação

Crie um diretório chamado `app` no mesmo diretório onde você criou o arquivo YML. Dentro deste diretório, crie um arquivo `index.html` com o conteúdo HTML básico, como um "Hello World":

```html
<!DOCTYPE html>
<html>
<head>
  <title>Minha Aplicação Web</title>
</head>
<body>
  <h1>Hello World! Este é o meu servidor Apache com Docker.</h1>
</body>
</html>
```

### 3. Subir o Arquivo YML e a Aplicação para um Repositório no GitHub

3.1. Inicialize um repositório Git no diretório onde estão os arquivos:

```bash
git init
```

3.2. Adicione os arquivos ao controle de versão e faça um commit:

```bash
git add .
git commit -m "Configuração inicial do servidor Apache"
```

3.3. Crie um repositório vazio no GitHub (sem README, .gitignore, etc.).

3.4. Conecte seu repositório local ao repositório no GitHub:

```bash
git remote add origin <URL_DO_SEU_REPOSITORIO>
git branch -M main
git push -u origin main
```

Agora você tem seu código no GitHub!

### 4. Implemente o Desafio e Suba seu Projeto

Aqui está um desafio para você: modifique o arquivo `index.html` para adicionar uma imagem ou estilização CSS à página. Após fazer as alterações, siga o mesmo processo de commit e push para atualizar seu repositório no GitHub.

Parabéns! Você configurou um servidor Apache usando Docker Compose, hospedou uma aplicação web simples e publicou tudo em um repositório no GitHub. Isso enriquece seu portfólio de projetos e demonstra suas habilidades.
<p> version: '3'
services:
  webserver:
    image: httpd:latest
    ports:
      - "80:80"
    volumes:
      - ./app:/usr/local/apache2/htdocs/
<p>
2. Especificar o Local dos Arquivos da Aplicação
Crie um diretório chamado app no mesmo diretório onde você criou o arquivo YML. Dentro deste diretório, crie um arquivo index.html com o conteúdo HTML básico, como um "Hello World":

html
Copy code
<!DOCTYPE html>
<html>
<head>
  <title>Minha Aplicação Web</title>
</head>
<body>
  <h1>Hello World! Este é o meu servidor Apache com Docker.</h1>
</body>
</html>

3. Subir o Arquivo YML e a Aplicação para um Repositório no GitHub
3.1. Inicialize um repositório Git no diretório onde estão os arquivos:

git init
3.2. Adicione os arquivos ao controle de versão e faça um commit:

```bash
git add .
git commit -m "Configuração inicial do servidor Apache"
3.3. Crie um repositório vazio no GitHub (sem README, .gitignore, etc.).

3.4. Conecte seu repositório local ao repositório no GitHub:


git remote add origin <URL_DO_SEU_REPOSITORIO>
git branch -M main
git push -u origin main
Agora você tem seu código no GitHub!