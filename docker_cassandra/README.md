# build and run
docker-compose up --build

# create keyspace
docker exec dockercassandra_web_1 python /code/createkeyspace.py

# acesss cassandra server
docker exec -t cassandra11 cqlsh
