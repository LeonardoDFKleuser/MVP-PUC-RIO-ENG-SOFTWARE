FROM python:3.11.5

# Crio e navego para o diretório de execução do projeto
RUN mkdir -p /usr/src/app/back
WORKDIR /usr/src/app/back

# Copio os arquivos do projeto e corrijo as permissões de acesso
COPY meu_app_api/ .
RUN chmod -R 777 ./

# https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/
# Configuro o ambiente do Python
RUN python3 -m venv env
RUN sh ./env/bin/activate

# Atualizo o pip do container
RUN python3 -m pip install --upgrade pip
RUN echo $(python3 -m pip --version)

# Instalo os pacotes do projeto
RUN python3 -m pip install -r requirements.txt

CMD [ "flask", "run", "--host", "0.0.0.0", "--debugger"]