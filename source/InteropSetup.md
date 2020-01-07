Step 1: Visit the AUVSI Interop repository for instructions regarding the setup of the Interoperability Server (https://github.com/auvsi-suas/interop)
    Note: When reviewing the prerequisites it is likely that the only thing you will need to install is Docker. For instructions on how to install Docker with Ubuntu see https://docs.docker.com/install/linux/docker-ce/ubuntu/
          After successfully installing the Docker Engine, install Docker Compose as listed in the instructions found at https://docs.docker.com/compose/install/

Step 2: Run the server by navigating to the interop/server folder and running "sudo ./interop-server.sh up" (the default address at which the server can then be accessed from a web browser is localhost:8000)

Step 3: Interact with the server using the client. Navigate to the interop/client folder and run "sudo ./interop-client.sh run", after which you can perform various tasks including getting the teams, the mission details, and so on.
