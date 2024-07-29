FROM python:3.10-slim-buster

#File inside new (different) OS
WORKDIR /backend-flask
#copy req file from old os to new os
COPY requirements.txt requirements.txt
#Install python 
RUN pip3 install -r requirements.txt
#copy from old os backend-flask to new os backend-flask
COPY . .
#set environment variables
ENV FLASK_ENV=development

EXPOSE ${PORT}
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]