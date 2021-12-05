# Docker-Snippets

  ## Docker Run Image

    docker container run <CONTAINER NAME>

  ## List Containers

    docker container ls -a

  ## List Images 

    docker image ls

  ## Start Container

    docker start <CONTAINER NAME>
    
  ## Run Container on PORT 3000
  
    docker run -dp 3000:3000 <CONTAINER NAME>

  ## Kill Container

    docker kill <CONTAINER NAME>

  ## Start Container in Interactive Mode

    docker start -i <CONTAINER NAME>

  ## DockerFile Example

    FROM node:16

    WORKDIR /usr/src/app

    COPY . .

    RUN npm ci

    CMD npm start
    

  ## Build Image using dockerfile

    docker build -t <CONTAINER NAME> .

  ## Docker Compose File Example

    version: '3.8'            # Version 3.8 is quite new and should work

    services:
      app:                    # The name of the service, can be anything
        image: express-server # Declares which image to use
        build: .              # Declares where to build if image is not found
        ports:                # Declares the ports to publish
          - 3000:3000

  ## Docker compose Build and Run Application

    docker-compose up

  ## Docker compose Rebuild Application

    docker-compose up --build

  ## Docker compose Run Application in the background

    docker-compose up -d

  ## Docker compose Close Application

    docker-compose down

