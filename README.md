# Docker-ELK-Filebeat

* A configuration lab for deploying Elastic-Logstash-Kibana with data collector Filebeat on Docker

## Docker

- Download and Install Docker at https://www.docker.com
- Command to set up the environment:

```
  docker-compose up
```
## Filebeat
* In the file filebeat.yml, there are codes for reading .log files and instant docker inputs 
* The docker inputs are live-running containers except running ELK containers since they have been supported by Kibana

## ELK

Ports used for config. :

- 5044: Logstash
- 9200: Elasticsearch
- 5601: Kibana

Type the localhost:5061 in the browser to go as an entry point to Kibana interface.
### .env
* Important is to declare the version in ELK and Filebeat in the .env with the environment variable, here in example is D_VERSION.
* The version used in this platform is 7.7.1
### Kibana
* Type the localhost:5061 in the browser to go as an entry point to Kibana interface.
* For default the id and password corresponding to "elastic" and "password".
* Remember to change reload in Kibana from default "last 15 minutes" to "Year to date" to observe the whole example .log data

## Example .log
The logs folder contains the example .log file.  
