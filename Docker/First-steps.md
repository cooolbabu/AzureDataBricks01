### Docker first steps

- docker container run hello-world
    - This will pull the hello-world container and run it locally

- docker images or docker image ls - to list images
- docker ps or docker container ls - to see running containers

- docker pull codewithpraveen/labs-docker-sql:1.0.0
- docker pull mcr.microsoft.com/mssql/server:2022-latest 
    - This image contains MS SQL Server 2022
    - BrezyWeather App API to test API interfaces

- To create a docker network
    '''
        docker network create brezy-network
        docker network ls

- Run the container
    '''
        docker run -d \
            -p 8080:80 \
            --name brezyweather-app \
            codewithpraveen/labs-docker-sql:1.0.0

        docker run -d \
            -e "ACCEPT_EULA=1" \
            -e "MSSQL_SA_PASSWORD=Password@123" \
            -p 1433:1433 \
            --network=brezy-network \
            --name=brezyweather-db \
            mcr.microsoft.com/mssql/server:2022-latest
    '''

- Enter the bash shell of the container, check connection to database
    '''
        docker exec -it brezyweather-db /bin/bash
        /opt/mssql-tools/bin/sqlcmd -S localhost -U SA -P Password@123
        SELECT name FROM sys.databases
        go

- Stop the container
    docker container stop brezyweather-app

- curl http://localhost:8080/weather | json_pp

- Cleanup - elete containers and images
    '''
        docker container rm -f $(docker container ls -a -q)
        docker image rm -f $(docker image ls -a -q)
        docker network rm brezy-network
        docker system df

- MLFlow
    '''
        docker run -d --name mlflow-container -e TZ=UTC -p 5000:5000 -p 5002:5002 ubuntu/mlflow:2.1.1_1.0-22.04

        


    