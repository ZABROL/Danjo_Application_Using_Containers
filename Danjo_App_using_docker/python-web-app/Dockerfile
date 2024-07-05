
Danjo Project Dockerfile

FROM ubuntu

WORKDIR /app

COPY requirements.txt /app
COPY devops /app

ENV PIP_BREAK_SYSTEM_PACKAGES 1
RUN apt-get update
RUN apt-get install -y 
RUN apt install pip -y
RUN pip install -r requirements.txt
RUN cd devops

ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]

