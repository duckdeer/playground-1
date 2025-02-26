# AsyncAPI Playground

![](screenshot.png)

## Using it locally

Run:

```
npm install
```

and

```
npm start
```

and go to [http://localhost:5000]().

## Build docker image

```
docker build -t asyncapi-playground .
```

## Run docker image

```
docker run -d --name asyncapi-playground -p 83:5000 asyncapi-playground:latest
```

Then browse to [http://localhost:83/]()

## URL query parameters:

- **load** - load the external AsyncAPI spec:

```
https://playground.asyncapi.io/?load=https://raw.githubusercontent.com/asyncapi/spec/master/examples/streetlights-kafka.yml
```

- **url** - this same purpose as **load**:

```
https://playground.asyncapi.io/?url=https://raw.githubusercontent.com/asyncapi/spec/master/examples/streetlights-kafka.yml
```

- **template** - show given template. Allowed values are `markdown` and `html`:

```
https://playground.asyncapi.io/?template=markdown
```

- **readOnly** - show only rendered template. Allowed values are `true` and empty string:

```
https://playground.asyncapi.io/?readOnly
```

## Environment variables:

- **DISABLE_DEBUG** - set it to 1 or `true` to disable logs:

```
DISABLE_DEBUG=1 npm start
```
