
tag=base
image_name=alpine-dev
name=fenggeorgeyu/${image_name}:${tag}
container_name=alpine1
all: build

build:
	docker build -t ${name} .
	docker tag ${name} fenggeorgeyu/${image_name}:latest

push:
	docker push ${name}
	docker push fenggeorgeyu/${image_name}:latest

clean:
	docker rmi ${name}

test: run

run:
	docker run -itd --name ${container_name} -v $$(pwd)/../shared:/shared ${name} bash	

bash:
	docker exec -it ${container_name} bash

stop:
	docker stop ${container_name}

delete:
	docker rm ${container_name}



