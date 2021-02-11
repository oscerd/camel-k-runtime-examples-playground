# camel-k-runtime-example-kafka-s3

build:
```shell script
./mvnw package
```

docker:
```shell script
docker run --rm -ti \
    -v $PWD/data:/etc/camel:Z \
    -e CAMEL_K_CONF=/etc/camel/application.properties \
    -e AWS_ACCESS_KEY=<access_key> \
    -e AWS_SECRET_KEY=<secret_key> \
    --network="host" \
    quay.io/oscerd/camel-k-runtime-example-kafka-s3:1.6.0-jvm
```

You'll need a running Kafka broker locally on your host.
