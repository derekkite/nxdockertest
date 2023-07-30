docker-compose -f docker-compose.single.yml up --build

to create a docker container that watches changes and rebuilds

docker-compose -f docker-compose.multiple.yml up --build

to create multiple docker containers that watch. Only one can run, the others error out. docker container ls
shows which is running. There are created, test-server, test-checkin, test-fileprocessing, test-sockets.
They do nothing, are simply scaffolding from nx create.

docker restart test-sockets will run that image, and the one running will error out and exit.
