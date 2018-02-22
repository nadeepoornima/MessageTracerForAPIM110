# The Sample Custom Handler to trace the message for APIM 1.10
This is a sample handler to trace the message on the APIM 1.10. The APIM 1.10, don't have a such message tracing feature. So this become an alternative solution to trace the message.

## Set up and Run

1. First clone the project
2. Export the project to your IDE through pom.xml
3. Build the Jar by executing the "mvn clean install"
4. Already run the server, then stop the server
5. Copy the Jar to the lib folder in the APIM 1.10(<APIM_HOME>/repository/component/lib)
6. Make sure to configure that handler on the synapse-handlers.xml (<APIM_HOME>/repository/conf) file as follows.
<handler name="MessageIDHandler" class="org.wso2.handler.synapse.MessageIDHandler"/>
7. The message logs are only showing when the "DUBUG" is enabled on the log4j.properties file. For that, please put the following code on the log4j.properties (<APIM_HOME>/repository/conf)file also.
log4j.logger.org.wso2.handler.synapse.MessageIDHandler=DEBUG
8. After doing the particular changes, please restart the server. 
