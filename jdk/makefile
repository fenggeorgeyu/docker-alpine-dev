
tag=jdk
image_name=alpine-dev
name=fenggeorgeyu/${image_name}:${tag}

all: build 

build:
	docker build -t ${name} .

push:
	docker push ${name}

clean:
	docker rmi ${name}



