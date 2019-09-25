# Exemplo de Dokerfile para empacotar a  aplicação Linux Dash (https://github.com/afaqurk/linux-dash) 

# Cria a imagem com base no Ubuntu
FROM ubuntu

# Eu sou o mantenedor do projeto
MAINTAINER Ricardo Robaina <ricardorobaina11@gmail.com>

# Atualiza o sistema e instala as dependências
RUN apt-get update
RUN apt-get install -y git
RUN apt-get install -y python

# Clona o diretório da aplicação
RUN git clone --depth 1 https://github.com/afaqurk/linux-dash.git

# Adiciona o diretório padrão
WORKDIR /linux-dash/app/server

# Expoem a porta 80 automaticamente
EXPOSE 80

# Starta a aplicação
CMD python index.py