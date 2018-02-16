## `words/wiktionary`

```js
const wiktionary = require('wiktionary')

wiktionary('somatology').then(result => {
  console.log(result)

  /*
  { query: 'somatology',
    html: '<p> ...same as text but with markup preserved... </p>',
    text: 'English\nEtymology\nFrom soma (body) +‎ -ology.\nNoun\nsomatology (usually uncountable, plural somatologies)\nThe study of the physical nature of human beings.\nDerived terms\nanthroposomatology\n' }
  */
})
```

## Frequency Lists

https://en.wiktionary.org/wiki/Wiktionary:Frequency_lists

@TODO: how to download without scraping?
