
# kafka-ansible

  To run: 

    $ansible-playbook install-kafka.yaml   

To adjust the **server.properties** settings, edit the ./vars/settings.yaml file.
properties follow the pattern: the prefix "kafka_" + original property with the character "." (dot)  edited to "_" (underline). 

Example:

    server.properties
         auto.create.topics.enable
    settings.yaml
         kafka_auto_create_topics_enable


There are 2  gropus of properties for **kafka.properties** in the file.

 -   KAFKA server.properties [1]: Common and default properties of
   server.properties original.
  
 -  KAFKA server.properties [2]: Extra settings for server.prperties. The
   relation of all properties can be visualized in the [kafka
   documentation](https://kafka.apache.org/documentation/).  In this 2nd group the properties are in a list called kafka_properties with 2 attributes:   
	- **key**: The name of property
	- **value**: The value of property. If the value is none the property is not included in server.properties.

## Tested

### Kafka Version

-  [kafka_2.12-2.4.1](https://www.apache.org/dyn/closer.cgi?path=/kafka/2.4.1/kafka_2.12-2.4.1.tgz)

  

-  [AMQ Streams 1.4.1](https://access.redhat.com/jbossnetwork/restricted/listSoftware.html?downloadType=distributions&product=jboss.amq.streams&version=1.4.1)

  

### Operation System:

- Red Hat Enterprise Linux Server release 7.8 (Maipo)
