# Kafka Streaming Platform on Docker

The environment for this course is completely based on docker containers. 

In order to simplify the provisioning, a single docker-compose configuration is used. All the necessary software will be provisioned using Docker.  

For Kafka we will be using the Docker images provided by Confluent and available under the following GitHub project: <https://github.com/confluentinc/cp-docker-images>. In this project, there is an example folder with a few different docker compose configuration for various Confluent Platform configurations.

You have the following options to start the environment:

 * [**Local Virtual Machine Environment**](./LocalVirtualMachine.md) - a Virtual Machine with Docker and Docker Compose pre-installed will be distributed at by the course infrastructure. You will need 50 GB free disk space.
 * [**Local Docker Environment**](./LocalDocker.md) - you have a local Docker and Docker Compose setup in place which you want to use
 * [**AWS Lightsail Environment**](./Lightsail.md) - AWS Lightsail is a service in Amazon Web Services (AWS) with which we can easily startup an environment and provide all the necessary bootstrapping as a script.

## Post Provisioning

These steps are necessary after the starting the docker environment. 

### Add entry to local `/etc/hosts` File

To simplify working with the Streaming Platform and for the links below to work, add the following entry to your local `/etc/hosts` file. 

```
40.91.195.92	streamingplatform
```

Replace the IP address by the public IP address of the docker host. 

## Services accessible on Streaming Platform
The following service are available as part of the platform:

Type | Service | Url
------|------- | -------------
Development | StreamSets Data Collector | <http://streamingplatform:28029>
Development | Apache NiFi | <http://streamingplatform:28054/nifi>
Development | Apache Zeppelin | <http://streamingplatform:28055>
Governance | Schema Registry UI  | <http://streamingplatform:28039>
Governance | Schema Registry Rest API  | <http://streamingplatform:28030>
Management | Kafka Connect UI | <http://streamingplatform:28038>
Management | Kafka Manager  | <http://streamingplatform:28044>
Management | Kafkahq  | <http://streamingplatform:28042>
Management | Zoonavigator  | <http://streamingplatform:28047>
Management | Mino | <http://streamingplatform:28083>
Management | Kafka Rest Service | <http://streamingplatform:28012>
Management | Kafka Connect Rest Service | <http://streamingplatform:28013>
Management | MQTT UI | <http://streamingplatform:28082>
Management | Portainer | <http://streamingplatform:28071>

