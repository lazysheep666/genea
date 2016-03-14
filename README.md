Genea
=======================

Genetic Algorithm for JavaScript.

### Installation

```bash
$ npm install genea --save
```

### Usage

```javascript
import Genea from "genea"

let ga = new Genea({
  geneLength: 15,
  mutateProbability: 0.5,
  doneFitness: 1,
  populationSize: 5,
  getFitness: function(gene) {
    var tar = 111111111100011
    return 1 - Math.abs(+gene - tar) / tar
  },
  done: function(gene) {
    console.log("Get Result:", gene)
  },
  onGeneration: function(generation, genes) {
    console.log(generation, genes)
  },
  outOfGenerationsSize: function(generations, fitnesses) {
    console.log(generations, fitnesses)
  }
})

ga.start()
```

## License

The MIT License (MIT)

Copyright (c) 2016 Livoras

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
