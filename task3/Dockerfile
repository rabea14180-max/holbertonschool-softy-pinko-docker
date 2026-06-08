FROM ubuntu:latest

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y python3 python3-pip

WORKDIR /app

COPY ./api.py /app/api.py

RUN pip3 install flask

CMD ["python3", "-m", "flask", "--app", "api", "run", "--host=0.0.0.0", "--port=5252"]
