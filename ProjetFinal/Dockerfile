# Image mariadb version 11
FROM mariadb:11

# Variables d'environement
# MYSQL_ROOT_PASSWORD : mot de passe pour l'utilisateur root
ENV MYSQL_ROOT_PASSWORD=esgi

# Copie du fichier sql depuis l'entrypoint
COPY /home/vullwen/ProjetFinal/init_db.sql /docker-entrypoint-initdb.d/

# Ouvre le port 3306 pour mariadb
EXPOSE 3306

# on lance au démarage cette comande
CMD ["mysqld"]

