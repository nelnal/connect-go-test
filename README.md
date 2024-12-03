# connect-go-test

## Setup

install buf

```bash
$ go install github.com/bufbuild/buf/cmd/buf@latest
```

```bash
$ docker compose build
$ docker compose up -d
```

## when changed proto files

generate go source files

```bash
$ buf registry login
$ buf generate
```
