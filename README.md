# Creating a Django environment on Docker
Baixando e instalando Docker
* curl -fsSL https://get.docker.com -o get-docker.sh
* sudo sh get-docker.sh

Verificar status do Docker
* docker -v
* service docker status
* sudo systemctl status docker

Adicionar usuário para utilizar o Docker sem privilégios root (necessário reiniciar sessão)
* sudo usermod -aG docker $(whoami)

Solução temporária para não precisar reiniciar sessão
* sg docker

Inicializar o cluster
* docker swarm init

Criar imagem
* docker build -t meusuario/nomedaminhaimagem:1.0 .

Criar Stack
* docker stack deploy -c docker-compose.yml NOMECONTAINER
