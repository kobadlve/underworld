# Under World 

underworld is a multi honeypot platform using docker.

It shows log of honeypots using ELK Stack(https://www.elastic.co/jp/elk-stack) and analyze it.

## Installation

1. Install Docker and Docker Compose

Docker needs at least 4GB memory

2. Start Docker

3. Clone this repository
```
$ git clone https://github.com/kobadlve/honeydirect.git
$ cd honeydirect
```

4. Build
```
$ docker-compose build
$ docker-compose up
```

Kibana running on http://localhost:5061

Please set index pattern to `logstash-*` and Time filter field name to `@timestame`

![kibana](https://github.com/kobadlve/honeydirect/blob/master/kibana.png)

## Running service

* ELK
  * Elasticsearch
  * Logstash
  * Kibana - http://localhost:5061
* Dionaea

### ELK Stack

ELK Stack composed by Elasticksearch, Logstash and Kibana.

### Honeypots

#### Dionaea

Dionaea is a low-interaction honeypot that captures attack payloads and malware. 
Dionaea is meant to be a nepenthes successor, embedding python as scripting language, using libemu to detect shellcodes, supporting ipv6 and tls. (https://www.honeynet.org/project/Dionaea)

Repository - https://github.com/DinoTools/dionaea

