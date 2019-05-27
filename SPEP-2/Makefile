IMAGE_NAME=simplepieng/docbuilder
RUN_CONTAINER=docker run -ti -v $$(pwd):/workspace $(IMAGE_NAME):latest

all:
	@cat Makefile | grep "^[a-z]" | sed 's/://'

#-------------------------------------------------------------------------------

.PHONY: build
build:
	# Use Docker to build the container.
	docker build --compress --force-rm --squash --tag $(IMAGE_NAME):latest .

.PHONY: clean
clean:
	# Remove the Docker container.
	docker image rm --force $(IMAGE_NAME):latest

.PHONY: rmint
rmint:
	# Remove the intermediate Docker containers. `make build` will start over from scratch.
	docker images | grep "<none>" | awk '{print $$3}' | xargs -P 2 -I% docker rmi -f %

#-------------------------------------------------------------------------------

.PHONY: chart
chart:
	$(RUN_CONTAINER) java -jar /usr/local/plantuml.jar -tsvg -charset UTF-8 -nbthread auto oneway-git-merges.uml
	$(RUN_CONTAINER) java -jar /usr/local/plantuml.jar -tpng -charset UTF-8 -nbthread auto oneway-git-merges.uml
