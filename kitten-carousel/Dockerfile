FROM nginx
RUN apt update -y
WORKDIR /usr/share/nginx/html
RUN rm index.html
COPY . /usr/share/nginx/html
EXPOSE 80


# https://hub.docker.com/repository/docker/cagatayakk/kitten-carousel

# docker run -d --name roman -p 80:80 cagatayakk/kitten-carousel

