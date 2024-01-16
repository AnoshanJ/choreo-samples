# Echo Service Using Python-Flask

## Use case

When the service is invoked with a message, the service will respond with the same message received on an HTTP POST.

## How to Run

`python -m pip install flask`
`python echo.py`
OR Using default port: 5000
`python -m flask --app echo run`

## Deploying the application in Choreo

1. Fork this repository.
2. Create a `Service` component in Choreo.
3. Select the 'Python' buildpack
4. Deploy the component.

## Testing the application

Invoke the following endpoints to test the application. Make sure to change the `<endpoint-url>` to the URL of the deployed component.

## Test the endpoint

```
curl -L '<endpoint-url>/echo' -H 'Content-Type: text/plain' -d '"Hello Word!"'
```

```
curl -L '<endpoint-url>/health'
```
