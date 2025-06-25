# Manual de Instalação

Este documento visa fornecer um guia com todos os procedimentos necessários para a execução do projeto final numa máquina local.

## Tabela de Contéudos

- Instalações e dependências necessárias
- Acesso ao código fonte do projeto
- Execução da interface gráfica
- Execução do serviço de API
- Execução do micro-serviço do Langflow

## Instalações e depêndencias necessárias

### Node.js 22.17.0

<img src="https://nodejs.org/static/images/logo.svg" width=300 style="border-radius: 12px"/>

O Node.js é essencial para executar este projeto. Faça o download da versão LTS (Long Term Support) mais recente:

[Download do NodeJS para Windows ou MacOS](https://nodejs.org/pt/download)

**Versão recomendada: 22.17.0**

### Docker Desktop

<img src="./docs/docker-desktop.svg" width=300 style="border-radius: 12px"/>

O Docker Desktop é necessário para executar o rabbitmq. Faça download da versão mais recente:

[Download para Windows](https://docs.docker.com/desktop/setup/install/windows-install)

[Download para MacOS](https://docs.docker.com/desktop/setup/install/mac-install/)

[Download para Linux](https://docs.docker.com/desktop/setup/install/linux/)

### Langflow Desktop

<img src="./docs/langflow.jpg" width=300 style="border-radius: 12px"/>

O Langflow é a plataforma utilizada para a criação e gestão de agentes AI, é necessário para a execução do projeto. Faça download da versão mais recente:

[Download para Windows ou MacOS](https://www.langflow.org/desktop)

É necessária uma conta no Langflow, pode criar a sua ao abrir a aplicação pela primeira vez.

### Git

<img src="./docs/git.png" width=300 style="border-radius: 12px"/>

O Git é a ferramenta usada para a gestão do código fonte do projeto, é necessária para obter acesso ao mesmo, instale a versão mais recente:

[Download para Windows, MacOS e Linux](http://git-scm.com/downloads)

É necessária uma conta de Git, se ainda não tem uma poderá ser necessário registar-se [aqui](https://github.com).

**Nota: Certifique-se que todas estas dependências estão corretamente instaladas antes de avançar para o próximo passo**

## Acesso ao código fonte

Este projeto encontra-se dividio em 3 reposítórios de github.

Interface Gráfica: http://github.com/spars57/aibpa-ui

Serviço: http://github.com/spars57/aibpa-service

Micro-Serviço Langflow: http://github.com/spars57/aibpa-langfow

Para obter acesso ao código fonte basta clonar o reposítório através dos seguintes passos.

1. Abrir o terminal com previlégios de administrador.
2. Verificar se tem o git instalado executando o comando: `git version`.
3. Criar uma pasta para guardar o código fonte através do comando: `mkdir fonte`.
4. Entrar na pasta através do comando: `cd fonte`
5. Clonar todo o código fonte executando os seguintes 3 comandos:

- `git clone http://github.com/spars57/aibpa-ui`
- `git clone http://github.com/spars57/aibpa-service`
- `git clone http://github.com/spars57/aibpa-langflow`

Após a execução destes comandos, ao entrar na pasta `fonte`deverá ver 3 pastas com os seguintes nomes: `aibpa-ui`, `aibpa-service`, `aibpa-langflow`.
