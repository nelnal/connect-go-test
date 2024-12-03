# connect-go-test

## Setup

install buf

```bash
$ go install github.com/bufbuild/buf/cmd/buf@latest
$ go install github.com/k1LoW/runn/cmd/runn@latest
```

## Test

launch server

```bash
$ docker compose up --build -d
```

run test

```bash
# call API by http
$ runn run book/rest/greet.yaml
(output)
# call API by gRPC
$ runn run --scopes read:parent book/grpc/greet.yaml
(output)
```

## when changed proto files

generate go source files from proto files

```bash
$ buf registry login
$ buf generate
```