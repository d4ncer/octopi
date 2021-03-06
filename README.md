# octopi.js

<img src='media/octopi.png' align='right'/>

Micro (0.5kB) trie based suggestion generating
library, made with autocompletion, control, and
a low memory footprint in mind. Check out the
[demo](https://eugene-eeo.github.io/octopi/demo.html).

```js
var oct = Octopi(['bird', 'boy']);
oct.add('bid', {'word': 'BID'});
oct.get('bi');   // => ['bird', {'word':'BID'}]
```

### Do you even normalise?

Octopi allows for arbitrary data to be associated
with words added to the tree. This means that you
have full control over normalisation of the words.
For example:

```js
word = 'CoolUseRName';
oct.add(word.toLowerCase(), word);
oct.get(word.toLowerCase());
```

### Installation

```sh
$ bower install eugenee-eeo/octopi
```
