# survey-rest-gateway
Act as a single entry application and responsible for dispatching the requests to other survey micro services
this is the only port which is exposed for public network and accepts requests from outside


# Some parts this service code is copied from my open source rest gateway 
<a href="https://github.com/JavaAdore/rest-gateway">https://github.com/JavaAdore/rest-gateway</a>


# prerequisites
survey eureka-server should be up and run<br/>
<a href="https://github.com/JavaAdore/eureka-server">https://github.com/JavaAdore/survey-eureka-server</a> <br/>


The following environment variables should be added

# SURVEY_EUREKA_SERVER_IP = 127.0.0.1

# SURVEY_REST_GATEWAY_PORT = 8080

 
# build
as root/Administration <br/>
mvn clean install docker:removeImage docker:build
# run
java -jar target/survey-rest-gateway.jar
