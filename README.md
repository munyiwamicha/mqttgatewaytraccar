Mqttgatewaytraccar
  

Mqttgatewaytraccar is a small Server written in NodeJs to use Traccar in other IoT Platforms such as Thingsboard
 

Mqttgatewaytraccar uses a number of open source projects to work properly:
  

*  [MQTT](https://www.npmjs.com/package/mqtt) - Node.JS client library for the MQTT protocol
*  [Micro](https://www.npmjs.com/package/micro) - Micro — Asynchronous HTTP microservices

# Setup and Starting via npm

```sh
npm install
npm start
```

# Setup and Starting via Docker-compose
##### !!! Dont forget Setup the var.env file for your environment !!!
```sh
nano docker-compose.yml
docker-compose up
```
 Try docker-compose up -d to start in background.


## Setup Traccar

On your Traccar Setup edit **conf/traccar.xml** and add forward

``` xml

<!-- position forwarding -->

<entry  key='forward.enable'>true</entry>
<entry  key='forward.json'>true</entry>
<entry  key='forward.url'>http://mqttgatewaytraccar_ip:8759/</entry>

```

**And restart Traccar Instance**

## Change Access Token to Id of Tracking Device

![deviceidasaccesstoken](https://user-images.githubusercontent.com/43235624/138587119-71a02117-de51-42b3-88c9-a8439b568444.png)

## Sample Telemetry

![telemetrydata](https://user-images.githubusercontent.com/43235624/138587162-71e47010-d32a-45dd-8c83-62a3a3a8969f.png)

## Sample Mobile Dashboard

![photo_2021-10-24_12-21-16](https://user-images.githubusercontent.com/43235624/138588109-4f9f1056-b063-4cb6-aaf3-0c1289abc888.jpg)

## Sample Dashboard
![smart tracking](https://user-images.githubusercontent.com/43235624/138588205-d6d1b648-a12b-4b81-87b6-51cb8c735959.png)




