Elasticsearch Quickstart
========================

This project produces a simple WAR that starts up an embedded elasticsearch cluster, useful
when enabling ES storage in the API Manager of apiman.

This quickstart will start up an elasticsearch cluster on the standard ES ports.  The cluster
name is "apiman" and the ES data will be stored in *standalone/data/es*.


Deployment
==========

To deploy this quickstart to a running WildFly 8.x server, simply execute the following commands:

----
cd apiman-quickstarts/elasticsearch
mvn clean install
mvn wildfly:deploy
----
