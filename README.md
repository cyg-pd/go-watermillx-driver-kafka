# go-watermillx-driver-kafka

[![tag](https://img.shields.io/github/tag/cyg-pd/go-watermillx-driver-kafka.svg)](https://github.com/cyg-pd/go-watermillx-driver-kafka/releases)
![Go Version](https://img.shields.io/badge/Go-%3E%3D%201.24-%23007d9c)
[![GoDoc](https://godoc.org/github.com/cyg-pd/go-watermillx-driver-kafka?status.svg)](https://pkg.go.dev/github.com/cyg-pd/go-watermillx-driver-kafka)
![Build Status](https://github.com/cyg-pd/go-watermillx-driver-kafka/actions/workflows/test.yml/badge.svg)
[![Go report](https://goreportcard.com/badge/github.com/cyg-pd/go-watermillx-driver-kafka)](https://goreportcard.com/report/github.com/cyg-pd/go-watermillx-driver-kafka)
[![Coverage](https://img.shields.io/codecov/c/github/cyg-pd/go-watermillx-driver-kafka)](https://codecov.io/gh/cyg-pd/go-watermillx-driver-kafka)
[![Contributors](https://img.shields.io/github/contributors/cyg-pd/go-watermillx-driver-kafka)](https://github.com/cyg-pd/go-watermillx-driver-kafka/graphs/contributors)
[![License](https://img.shields.io/github/license/cyg-pd/go-watermillx-driver-kafka)](./LICENSE)

## 🚀 Install

```sh
go get github.com/cyg-pd/go-watermillx-driver-kafka@v1
```

This library is v1 and follows SemVer strictly.

No breaking changes will be made to exported APIs before v2.0.0.

## 💡 Usage

You can import `go-watermillx-driver-kafka` using:

```go
package main

import (
	_ "github.com/cyg-pd/go-watermillx"
	"github.com/cyg-pd/go-watermillx-driver-kafka"
)

func main() {
	drv, err := driver.New("kafka", `{"Brokers": ["localhost:9092"], "InitializeTopicDetails":{"NumPartitions": 3}}`)
	if err != nil {
		panic(err)
	}

	pub, err := drv.Publisher()
	if err != nil {
		panic(err)
	}

	sub, err := drv.Subscriber()
	if err != nil {
		panic(err)
	}
}
```
