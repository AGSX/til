# Getting Started with Celery

**Date: June 9, 2016**

Celery is a task queue, which means it is a tool used to distribute tasks across several servers.

#### Brokers
Celery uses brokers to mediate between clients and workers. There are several choices available for brokers:
- RabbitMQ
- Redis
- Using a database
  - Using SQLAlchemy
  - Using the DJango database
- Other brokers
  - Amazon SQS
  - MongoDB
  - IronMQ

#### Installing Celery
```
pip install celery
```

#### Creating a Celery instance
```
app = Celery('module_name', backend='redis://localhost', broker='redis://localhost')
```
The first argument to a Celery instance is the module name, next is the backend argument wherein Celery stores or sends the states, and last is the broker keyword that specifies the URL of the message broker.

#### Running a worker server
```
celery -A tasks worker --loglevel=info
```

#### References:
- [First Steps with Celery](http://docs.celeryproject.org/en/latest/getting-started/first-steps-with-celery.html)
