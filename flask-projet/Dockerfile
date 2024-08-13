FROM python:3.12-slim

# workin directory in the container

WORKDIR /app

COPY . /app

# install the dependencies in  the container

RUN pip install -r  requirements.txt

EXPOSE 3000


# Command to run the app

CMD python ./main.py
