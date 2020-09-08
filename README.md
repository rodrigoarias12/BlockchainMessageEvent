# Using tye with rabbitmq 


```Configure tye.yaml
name: blockchainmessageevent
services:
- name: microservicemessagepub
  project: MicroServiceMessagePub/MicroServiceMessagePub.csproj
- name: microservicebackendsub
  project: MicroServiceBackEndSub/MicroServiceBackEndSub.csproj
- name: rabbit
  image: rabbitmq:3-management
  bindings:
    - name: ui
      protocol: http
      port: 15672
      containerPort: 15672
    - name: amqp
      protocol: amqp
      port: 5672
```
