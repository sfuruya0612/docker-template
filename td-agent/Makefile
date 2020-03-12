build:
	docker-compose build

up: build
	docker-compose up -d

down:
	docker-compose down -v

.PHONY: td-agent
td-agent: td-agent2 td-agent3

.PHONY: td-agent2
td-agent2:
	docker build -t ubuntu16.04-td-agent2:latest ./td-agent2/

.PHONY: td-agent3
td-agent3:
	docker build -t ubuntu16.04-td-agent3:latest ./td-agent3/
