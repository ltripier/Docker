Exo 1 :

    -docker pull docsseo91/stardocker:v1

Exo 2 :

    -docker build -t hylianmnst/coursdockerexo2 . 
    -docker run -d -p 1000:80 hylianmnst/coursdockerexo2

Exo 3 :

    -docker login
    -docker push hylianmnst/coursdockerexo2  

Exo 4 :

    -docker build -t hylianmnst/coursdockerexo4 .  
    -docker run -d -p 3001:3001 hylianmnst/coursdockerexo4

Exo 5 :

    - docker build -t hylianmnst/coursdockerexo5 .
    -docker run -d -p 5432:5432 -e POSTGRES_PASSWORD=postgres -e POSTGRES_USER=postgres --name coursdockerexo5 hylianmnst/coursdockerexo5
    -docker exec -it coursdockerexo5 bash
    -psql -h localhost -U postgres
    -SELECT nom FROM personnes WHERE age>30;
     nom
    -----------
    Charlie
    Erik
    Fanny
    George
    Karl
    Laura
    Mohamed
    Oscar
    Steve
    Tina
    Valerie
    William
    Xavier
    Zoé
    André
    Brigitte
    Danielle
    Flore
    Hugo
    Jocelyn
    (et d'autres... (54 au total))

Exo 6 :

    -docker network create -d bridge coursdockerexo6

    -docker build -t hylianmnst/coursdockerexo6 .  
    -docker run -d -p 3000:3000 --network=coursdockerexo6 hylianmnst/coursdockerexo6

    -docker run -d -p 5432:5432 -e POSTGRES_PASSWORD=postgres -e POSTGRES_USER=postgres --name coursdockerexo5 hylianmnst/coursdockerexo5


