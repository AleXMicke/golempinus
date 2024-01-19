# GoLemPinus

This project is a dictionary based lemmatizer written in go. 

Since v4 all dictionaries need to be gotten individually.

```
go get github.com/Ernesto-Che-Guevara/golempinus/v4
```


### What?

A [lemmatizer](https://en.wikipedia.org/wiki/Lemmatisation) is a tool that finds the base form of words.

| Lang    | Input      | Output  |
| ------- | ---------- | ------- |
| English | aligning   | align   |
| Swedish | sprungit   | springa |
| French  | abattaient | abattre |

It's based on the dictionaries found on [michmech/lemmatization-lists](https://github.com/michmech/lemmatization-lists), which are available under the [Open Database License](https://opendatacommons.org/licenses/odbl/summary/). This project would not be feasible without them.

### Languages

At the moment golem supports English, Swedish, French, Spanish, Italian & German, but adding another language should be no more trouble than getting the dictionary for that language. Some of which are already available on lexiconista. Please let me know if there is something you would like to see in here, or fork the project and create a pull request.

RUSSIAN!!!
```
go get github.com/Ernesto-Che-Guevara/golempinus/v4/dicts/ru
```


### Basic usage

```golang
package main

import (
	"fmt"

	"github.com/Ernesto-Che-Guevara/golempinus/v4"
	"github.com/Ernesto-Che-Guevara/golempinus/v4/dicts/ru"
)

func main() {
	// the language packages are available under golem/dicts
	// "en" is for english
	lemmatizer, err := golempinus.New(ru.New())
	if err != nil {
		panic(err)
	}
	word := lemmatizer.Lemma("ветра")
	fmt.Print(word)
}
```

### Contributors

- axamon
- charlesgiroux
- glaslos
