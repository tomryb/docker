# instalacja docker-compose

- https://docs.docker.com/compose/install/

# odpalenie docker-compose

- docker-compose up -d
- docker ps -a
- check localhost:8000
- docker exec -it mysql_database bash
- cd /var/lib/mysql --> ls
- docker run -it --link mysql_database:mysql --rm mysql sh -c 'exec mysql -h"$MYSQL_PORT_3306_TCP_ADDR" -P"$MYSQL_PORT_3306_TCP_PORT" -uroot -p"$MYSQL_ENV_MYSQL_ROOT_PASSQORD"'
- docker network connect bridge mysql_database
- no i bawimy się w mysql

 # przydatne komendy w docker-compose

 - docker-compose images
 - docker-compose config
 - docker-compose logs
 - docker-compose logs --tail=10