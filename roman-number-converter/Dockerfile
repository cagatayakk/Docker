FROM ubuntu
RUN apt-get update -y
RUN apt-get install python3 -y
RUN apt-get install python3-pip -y
RUN pip3 install flask
COPY . /app
WORKDIR /app
CMD python3 ./main.py

# https://hub.docker.com/repository/docker/cagatayakk/roman-number-converter 

#docker run -d --name roman -p 80:80 cagatayakk/roman-number-converter 
