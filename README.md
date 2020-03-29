![](https://github.com/OpenLiberty/open-liberty/blob/master/logos/logo_horizontal_light_navy.png)

The sample application contains a system microservice to retrieve the system properties and uses MicroProfile Config to simulate the status of the microservice, MicroProfile Health to determine the health of the microservice, and MicroProfile Metrics to provide metrics for the microservice.

This original sample from Liberty Gihub repository has been adapted to work with Okteto.

## Run Sample application (press [ENTER] key to run tests])
    mvn liberty:dev

### Open URL in browser
    http://localhost:9080

### Stop server (quit)
    q [ENTER]

## Using Okteto

In your dev machine deploy `k8s.yml` to set 9080 as the service port and start okteto remote dev environment:

```sh
kubectl apply -f k8s.yml
okteto up
```
Once inside your okteto remote shell you can start Liberty in dev mode (hot reloading classes and configs):

```sh
mvn liberty:dev -DserverStartTimeout=120
```
