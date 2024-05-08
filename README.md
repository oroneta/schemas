# Oroneta Project Services List

### DRONE-FRONT

Frontend part [view](https://github.com/oroneta/drone-front)

Services:
* Server: **[:80]** Apache Ngix With PHP serving React Build App
* React Development Server: **[:3000]** `npm run start` to execute server
* MySQL Database: **[:3306]** 
* PHPMyAdmin: **[:8081]** Must be disabled in production mode

### DRONE-MODULE

Manager, API and IA part [view](https://github.com/oroneta/drone-module)

Services:
* API Server: **[:60001]** API service to interact with **drone-front**
* MANAGER Server: **[:60002]** Brain of every drone
* AI Server: **[:60003]** Eye of every drone
* MongoDB Database: **[:27017]**
* Mongo-Express: **[:8081]** Must be disabled in production mode

### CORE-SYSTEM

Core algorythm and Drone bank [view](https://github.com/oroneta/core-system)

Services:
* Core Server: **[:60000]** 
* PostgreSQL Database: **[:5432]**
* Adminer: **[:8081]** Must be disabled in production mode



## Docs version
```log
*** CHANGELOG ***
v1-alpha [Actual version]
  * Changed ADMP to MavLink protocol
  * Added database diagram
---------------------------
v1-beta
```
