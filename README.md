# README

## Spring Boot Simple Customer Microservice

Eureka is a REST (Representational State Transfer) based service that is primarily used in the AWS cloud for locating services for the purpose of load balancing and failover of middle-tier servers. We call this service, the Eureka Server. Eureka also comes with a Java-based client component,the Eureka Client, which makes interactions with the service much easier. The client also has a built-in load balancer that does basic round-robin load balancing. At Netflix, a much more sophisticated load balancer wraps Eureka to provide weighted load balancing based on several factors like traffic, resource usage, error conditions etc to provide superior resiliency.

This project is a simple but functional example of Eureka Server using Spring Cloud with NO Authentication. 

### How to install
It's an eclipse project, just import it and run. If you want to run cluster please use Spring profiles **primary** and **secondary**.

### Parameters & Configuration
* **application.yml**
  * **server.port** : Server Port

### How to test

1. Configure application (application.yml above)
2. Start Eureka Server [rigth-clic, run  :) ]
3. Browse to *http://localhost:17001* (modify this URI according to configuration)
   In section "Instances currently registered with Eureka" you have to found **MYAPP-EUREKA-SINGLE-SERVER** server register
   You can start a cluster using Spring profiles **primary** and **secondary**, in that case you will found **MYAPP-EUREKA-SERVER** server register
4. Start at least one instance of [Customers Microservice](https://github.com/mariocuellar1/customers-simple-microservice) and [Vehicles Microservice](https://github.com/mariocuellar1/vehicles-simple-microservice)
5. Verify in *http://localhost:17001* section "Instances currently registered with Eureka" **CUSTOMERS-MICROSERVICE** and **VEHICLES-MICROSERVICE** appears.


And you Done !!!!  

### Notes:
- Please feel free to add/modify/correct/update any part of this content as necessary

### Related Projects
- [Customers Microservice](https://github.com/mariocuellar1/customers-simple-microservice)
- [Vehicles Microservice](https://github.com/mariocuellar1/vehicles-simple-microservice)

### Other Projects:
- [oAuth Server using oauth and opaque token](https://github.com/mariocuellar1/oauth-server-opaque)
- [Basic Resource Server using oauth and opaque token](https://github.com/mariocuellar1/basic-resource-server-opaque)
- [oAuth Server using JWT Token](https://github.com/mariocuellar1/oauth-server-jwt)
- [Basic Resource Server validating JWT Token](https://github.com/mariocuellar1/basic-resource-server-jwt)
