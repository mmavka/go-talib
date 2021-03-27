# go-talib

[![GoDoc](http://godoc.org/github.com/bozzo/go-talib?status.svg)](http://godoc.org/github.com/bozzo/go-talib) 

A pure [Go](http://golang.org/) port of [TA-Lib](http://ta-lib.org)

## Install

Require the package in your go.mod:

```go.mod
require github.com/bozzo/go-talib latest
```

Import it with:

```go
import "github.com/bozzo/go-talib"
```

and use `talib` as the package name inside the code.

## Example

```go
package main

import (
	"fmt"
	"github.com/markcheno/go-quote"
	"github.com/bozzo/go-talib"
)

func main() {
	spy, _ := quote.NewQuoteFromYahoo("spy", "2016-01-01", "2016-04-01", quote.Daily, true)
	fmt.Print(spy.CSV())
	rsi2 := talib.Rsi(spy.Close, 2)
	fmt.Println(rsi2)
}
```

## License

MIT License  - see LICENSE for more details

## Projects using this library

- [Golang Crypto Trading Bot](https://github.com/saniales/golang-crypto-trading-bot) by [saniales](https://github.com/saniales)

# Contributors

- [Markcheno](https://github.com/markcheno) 
- [Alessandro Sanino AKA saniales](https://github.com/saniales)
