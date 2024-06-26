FROM python:3.11.5

WORKDIR /usr/src/app/back

COPY . .

RUN python3 -m venv env

RUN env/Scripts/activate

RUN (env)$ pip install -r requirements.txt

CMD [ "flask", "run --host 0.0.0.0"]