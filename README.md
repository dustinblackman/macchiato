# Macchiato

[![Documentation][godoc-img]][godoc-url] ![License][license-img]

A mocha inspired reporter for [Ginkgo](https://onsi.github.io/ginkgo/)

[![Macchiato][macchiato-img]][macchiato-url]

## Usage

In your Ginkgo Suite, you can import *Macchiato* and use it as follows:

```go
package books_test

import (
	"testing"

	"github.com/crowley-io/macchiato"
	"github.com/onsi/ginkgo"
	"github.com/onsi/gomega"
)

func TestBooks(t *testing.T) {
	gomega.RegisterFailHandler(ginkgo.Fail)
	macchiato.RunSpecs(t, "Books Suite")
}
```

## Under the hood

`RunSpecs` will run Ginkgo with `RunSpecsWithCustomReporters` by injecting a Macchiato's `Reporter`.

## License

This is Free Software, released under the [`MIT License`](LICENSE).

[macchiato-url]: https://github.com/crowley-io/macchiato
[macchiato-img]: https://raw.githubusercontent.com/crowley-io/macchiato/master/macchiato.jpg
[godoc-url]: https://godoc.org/github.com/crowley-io/macchiato
[godoc-img]: https://godoc.org/github.com/crowley-io/macchiato?status.svg
[license-img]: https://img.shields.io/badge/license-MIT-blue.svg
