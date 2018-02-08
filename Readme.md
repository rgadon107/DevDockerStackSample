# Converting your DEV Environment to a Docker Stack

To start this basic LEMP stack:\
```docker stack deploy -c docker-compose.yml sunshine```

To take the stack down\
```docker stack rm sunshine```

Sample Web Folder:
 * _public_html/_ : This folder is mapped to the container and will update as you modify the files within it directly.

Sample docker-compose files:
 * _docker-compose.yml_ : Basic LEMP stack
 * _docker-compose-clientA.yml_ : Modified stack for client with alternate php version
 * _docker-compose-with-selenium.yml_ : LEMP stack with services defined for chrome and firefox selenium images
 
Additional Files:
 * _mysite.conf_ : Sample nginx configuration for this application
 * _root_db_password.txt_ : Secret file for the mysql image
 * _composer.json_ : Sample composer file 
 
### Note: Want to use composer? It doesn't need to be in your stack or installed locally
See https://store.docker.com/images/composer \
```docker run --rm -it --volume $PWD:/app composer install```
