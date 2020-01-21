FROM python:latest
RUN mkdir /app
COPY . /app
WORKDIR /app
RUN pip install -r requirements.txt
ENV FLASK_ENV='docker'
EXPOSE 80
CMD flask run --host=0.0.0.0 --port=80