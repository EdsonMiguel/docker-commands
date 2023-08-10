
# Comandos Docker

## Gerenciamento de Imagens

### Pull de Imagem

- **Descrição**: Baixa uma imagem do Docker Hub ou de um registro personalizado.
- Comando: `docker pull [imagem]`

## Criação e Execução de Contêineres

### Criar e Executar Contêiner

- **Descrição**: Cria e inicia um novo contêiner a partir de uma imagem.
- Comando: `docker run [imagem]`

### Criar e Executar Contêiner Interativo

- **Descrição**: Cria e inicia um novo contêiner em modo interativo com um shell de terminal.
- Comando: `docker run -it [imagem]`

### Criar e Executar Contêiner em Segundo Plano

- **Descrição**: Cria e inicia um novo contêiner em segundo plano (detach mode).
- Comando: `docker run -d [imagem]`

### Criar e Executar Contêiner com Mapeamento de Porta

- **Descrição**: Cria e inicia um novo contêiner, mapeando uma porta do host para uma porta no contêiner.
- Comando: `docker run -p [porta_host]:[porta_contêiner] [imagem]`

### Lidar com Volumes

#### Criar Contêiner com Volume

- **Descrição**: Cria e inicia um novo contêiner com um volume montado.
- Comando: `docker run -v [caminho_host]:[caminho_contêiner] [imagem]`

#### Listar Volumes

- **Descrição**: Lista todos os volumes disponíveis no sistema local.
- Comando: `docker volume ls`

### Gerenciamento de Contêineres

#### Listar Contêineres em Execução

- **Descrição**: Lista todos os contêineres em execução no momento.
- Comando: `docker ps`

#### Listar Todos os Contêineres

- **Descrição**: Lista todos os contêineres, incluindo os que não estão em execução.
- Comando: `docker ps -a`

#### Parar Contêiner

- **Descrição**: Interrompe um contêiner em execução.
- Comando: `docker stop [id_contêiner]` ou `docker stop [nome_contêiner]`

#### Iniciar Contêiner

- **Descrição**: Inicia um contêiner previamente parado.
- Comando: `docker start [id_contêiner]` ou `docker start [nome_contêiner]`

#### Reiniciar Contêiner

- **Descrição**: Reinicia um contêiner.
- Comando: `docker restart [id_contêiner]`

#### Remover Contêiner

- **Descrição**: Remove um contêiner específico.
- Comando: `docker rm [id_contêiner]`

#### Remover Contêiner Forçadamente

- **Descrição**: Remove um contêiner específico forçadamente.
- Comando: `docker rm -f [id_contêiner]`

### Lidar com Redes

#### Criar Rede

- **Descrição**: Cria uma nova rede personalizada.
- Comando: `docker network create [nome_rede]`

#### Listar Redes

- **Descrição**: Lista todas as redes disponíveis no sistema local.
- Comando: `docker network ls`

#### Conectar Contêiner a Rede

- **Descrição**: Conecta um contêiner a uma rede existente.
- Comando: `docker network connect [nome_rede] [nome_contêiner]`

#### Desconectar Contêiner de Rede

- **Descrição**: Desconecta um contêiner de uma rede.
- Comando: `docker network disconnect [nome_rede] [nome_contêiner]`

## Outros Comandos Úteis

### Construir Imagem

- **Descrição**: Constrói uma imagem a partir de um Dockerfile presente no diretório atual.
- Comando: `docker build .`

### Listar Imagens

- **Descrição**: Lista todas as imagens disponíveis no sistema local.
- Comando: `docker image ls`

### Remover Imagem

- **Descrição**: Remove uma imagem específica.
- Comando: `docker rmi [imagem]`

### Copiar entre Host e Contêiner

- **Descrição**: Copia arquivos ou diretórios entre o host e um contêiner.
- Comando: `docker cp [origem]:[destino]`

### Visualizar Processos em Execução

- **Descrição**: Exibe os processos em execução em um contêiner.
- Comando: `docker top [id_contêiner]`

### Inspecionar Contêiner

- **Descrição**: Exibe informações detalhadas sobre um contêiner.
- Comando: `docker inspect [id_contêiner]`

### Estatísticas de Uso de Recursos

- **Descrição**: Exibe estatísticas de uso de recursos de um contêiner.
- Comando: `docker stats [id_contêiner]`

### Acessar Shell Interativo em um Contêiner

- **Descrição**: Acessa um shell interativo dentro de um contêiner em execução.
- Comando: `docker exec -it [nome_contêiner] /bin/bash`

Lembre-se de substituir `[imagem]`, `[id_contêiner]`, `[nome_contêiner]`, `[porta_host]`, `[porta_contêiner]`, `[caminho_host]`, `[caminho_contêiner]`, `[nome_rede]` e outros valores pelos correspondentes à sua situação.
