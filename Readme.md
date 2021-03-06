*This repository is a mirror of the [component](http://component.io) module [matthewmueller/frequency-list](http://github.com/matthewmueller/frequency-list). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/matthewmueller-frequency-list`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# frequency-list

  Create frequency lists

## Example

```js
var FrequencyList = require('frequency-list'),
    list = new FrequencyList;

list.add('hi')
    .add('how are you')
    .add('whats up')
    .add('hi');

list.has('how are you') // true
list.size('hi') // 2
list.size('oh no') // 0

list.remove('hi')
list.unique('hi') // true
```

## Installation

    $ component install matthewmueller/frequency-list

## API

### FrequencyList( [values] )

Initialize the `FrequencyList` with an optional array of `values`

### #add(str)

Add a word or phrase to the frequency list

### #remove(str)

Remove a word or phrase from the frequency list.

### #has(str)

Checks to see if a word or phrase exists in the list.

### #size(str)

Gets the number of occurences of the given `str`. If the string is not in the list, the size will be 0.

### #unique(str)

Returns true if `str` occurs exactly once. Alias for `size(str) === 1`.

### #values()

Returns the raw frequency list. You may also use the alias `toJSON()`.

```js
list.values(); //=> { 'hi' : 2, 'how are you' : 1, 'whats up' : 1 }
```

## License

  MIT
