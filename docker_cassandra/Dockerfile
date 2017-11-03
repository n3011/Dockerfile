FROM python:3.5.0-slim

ADD requirements.txt requirements.txt
RUN pip install -r requirements.txt 

## run the app 
ADD app.py app.py

ADD . /code
WORKDIR /code
## expose the port
EXPOSE 5000

## start the command
CMD ["python", "app.py"]
