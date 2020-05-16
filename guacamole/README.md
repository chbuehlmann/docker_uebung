docker run --rm guacamole/guacamole /opt/guacamole/bin/initdb.sh --postgres > initdb.sql
docker run -d --name some-postgres -e POSTGRES_USER=guacamole_user -e POSTGRES_PASSWORD=some_password -v /home/cb/dev/docker_uebung/guacamole/initdb.sql:/docker-entrypoint-initdb.d/initdb.sql postgres
docker run -d --name some-guacd guacamole/guacd
docker run --name some-guacamole --link some-guacd:guacd     --link some-postgres:postgres          -e POSTGRES_DATABASE=guacamole_user      -e POSTGRES_USER=guacamole_user        -e POSTGRES_PASSWORD=some_password     -d -p 8080:8080 guacamole/guacamole

#http://localhost:8080/guacamole/ user: guacadmin passwort: guacadmin
