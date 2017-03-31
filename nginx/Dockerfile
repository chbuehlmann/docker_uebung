FROM stackbrew/debian:jessie
MAINTAINER Christoph Bühlmann <christoph.buehlmann@gibb.ch>;
RUN apt-get -q update
RUN apt-get -qy install nginx
ADD index.html /var/www/html/
EXPOSE 80
CMD ["nginx", "-g", "daemon off;" ]