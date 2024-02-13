# dcker-vYSY3u5F
docker compose -f docker-compose.yml up --build -d

# getting the root password:
# - run docker
# issue command
# > docker logs <db_container_name> 2>&1 | grep GENERATED
# should print out something like:
# >[Note] [Entrypoint]: GENERATED ROOT PASSWORD: OhUcVg+kpQRKmu0ZHvHkiLvlA9nkHIyL
mysql: 
root : OhUcVg+kpQRKmu0ZHvHkiLvlA9nkHIyL