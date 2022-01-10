---
title: Kafka (Message queue service)
slug: kafka
section: Services
---

**Last updated 7th January 2022**


## Objective  

Apache Kafka is an open-source stream-processing software platform.


It is a framework for storing, reading and analyzing streaming data. See the [Kafka documentation](https://kafka.apache.org/documentation) for more information.

## Supported versions

| **Grid** |  **Dedicated Generation 3** |
|----------------------------------|  
|  2.1 |  
|  2.2 |  
|  2.3 |  
|  2.4 |  
|  2.5 |  

## Relationship

The format exposed in the ``$PLATFORM_RELATIONSHIPS`` [environment variable](../../development-variables#platformsh-provided-variables):

```json  
{
    "service": "kafka25",
    "ip": "169.254.209.147",
    "hostname": "t7lv3t3ttyh3vyrzgqguj5upwy.kafka25.service._.eu-3.platformsh.site",
    "cluster": "rjify4yjcwxaa-master-7rqtwti",
    "host": "kafka.internal",
    "rel": "kafka",
    "scheme": "kafka",
    "type": "kafka:2.5",
    "port": 9092
}
```  

## Usage example

In your ``.platform/services.yaml``:


```yaml   
queuekafka:
    type: kafka:2.5
    disk: 512
```  


In your ``.platform.app.yaml``:


```yaml   
relationships:
    kafkaqueue: "queuekafka:kafka"
```  




You can then use the service in a configuration file of your application with something like:

> [!tabs]      
> Java     
>> ``` java     
>> {!> web/web-paas/static/files/fetch/examples/java/kafka !}  
>> ```     
> Python     
>> ``` python     
>> {!> web/web-paas/static/files/fetch/examples/python/kafka !}  
>> ```     
> Ruby     
>> ``` ruby     
>> 
>> ## With the ruby-kafka gem
>> 
>> # Producer
>> require "kafka"
>> kafka = Kafka.new(["kafka.internal:9092"], client_id: "my-application")
>> kafka.deliver_message("Hello, World!", topic: "greetings")
>> 
>> # Consumer
>> kafka.each_message(topic: "greetings") do |message|
>>   puts message.offset, message.key, message.value
>> end
>> 
>> ```     

(The specific way to inject configuration into your application will vary. Consult your application or framework's documentation.)
