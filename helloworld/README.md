# nameko-minimal
nameko minimal working example

## Requirements

- pipenv 
- Docker

## Start up

Install Nameko and start a virtual environment with
```
pipenv install nameko
pipenv shell
```

Start RabbitMQ to have an AMQP running for Nameko
```
docker run -d -p 5672:5672 rabbitmq:3
```

Open another terminal, start another virtual environment and enter nameko shell to test the greeting service
```
# From another terminal
pipenv shell
nameko shell
>>> n.rpc.greeting_service.hello(name="Alice")
```

