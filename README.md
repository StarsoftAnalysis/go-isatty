# go-isatty

[![Godoc Reference](https://godoc.org/github.com/starsoftanalysis/go-isatty?status.svg)](http://godoc.org/github.com/starsoftanalysis/go-isatty)
[![Codecov](https://codecov.io/gh/starsoftanalysis/go-isatty/branch/master/graph/badge.svg)](https://codecov.io/gh/starsoftanalysis/go-isatty)
[![Coverage Status](https://coveralls.io/repos/github/starsoftanalysis/go-isatty/badge.svg?branch=master)](https://coveralls.io/github/starsoftanalysis/go-isatty?branch=master)
[![Go Report Card](https://goreportcard.com/badge/starsoftanalysis/go-isatty)](https://goreportcard.com/report/starsoftanalysis/go-isatty)

isatty for golang

## Usage

```go
package main

import (
	"fmt"
	"github.com/starsoftanalysis/go-isatty"
	"os"
)

func main() {
	if isatty.IsTerminal(os.Stdout.Fd()) {
		fmt.Println("Is Terminal")
	} else if isatty.IsCygwinTerminal(os.Stdout.Fd()) {
		fmt.Println("Is Cygwin/MSYS2 Terminal")
	} else {
		fmt.Println("Is Not Terminal")
	}
}
```

## Installation

```
$ go get github.com/starsoftanalysis/go-isatty
```

## License

MIT

## Author

Yasuhiro Matsumoto (a.k.a starsoftanalysis)

## Thanks

* k-takata: base idea for IsCygwinTerminal

    https://github.com/k-takata/go-iscygpty
