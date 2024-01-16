# Echo Service Using Java-SpringBoot

## Use case

When the service is invoked with a message, the service will respond with the same message received via an HTTP POST.

## How to Run

`mvn clean compile package
`
`java -jar ./target/echo-service-0.0.1-SNAPSHOT.jar`

## Build the project

`./mvnw clean install`
Run the service

`./mvnw spring-boot:run`

## Deploying the application in Choreo

1. Fork this repository.
2. Create a `Service` component in Choreo.
3. Select the 'Docker' buildpack
4. Deploy the component.

#### Use the following build config when creating this component in Choreo:

- Build Preset: **Dockerfile**
- Dockerfile Path: `java-echo-service/Dockerfile`
- Docker Context Path: `java-echo-service`

The [endpoints.yaml](.choreo/endpoints.yaml) file contains the endpoint configurations that are used by the Choreo to expose the service.

## Testing the application

Invoke the following endpoints to test the application. Make sure to change the `<endpoint-url>` to the URL of the deployed component.

## Test the endpoint

```
curl -L '<endpoint-url>/echo' -H 'Content-Type: text/plain' -d '"Hello Word!"'
```

```
curl -L '<endpoint-url>/health'
```
