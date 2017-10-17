# save-case-dialog

A Polymer Element showing a dialog to save a document, entity, or search in a case using a profile manager.

### Example
```js
var buildPopupDataFunction = function(data, config) {
  return Object.keys(data).reduce(function(output, key) {
    output[config[key]] = data[key];
    return output;
  }, {});
};

var cases = [{
  name: 'Case 1'
}, {
  name: 'Case 2'
}];

var functionConfig = {
  key1: 'Field 1',
  key2: 'Field 2'
};

var networkExpansionParameters = {
  key1: true
};

var searchParameters = {
  key1: ['value1'],
  key2: ['value2', 'value3', 'value4']
};
```

```html
<save-search-dialog
  build-popup-data-function="[[buildPopupDataFunction]]"
  cases="[[cases]]"
  function-config="[[functionConfig]]"
  network-expansion-parameters="[[networkExpansionParameters]]"
  profile-manager="[[profileManager]]"
  search-parameters="[[searchParameters]]"
  user-id="1234">
</save-search-dialog>
```

### Dependencies

Dependencies are installed using [Bower](http://bower.io/):

    npm install -g bower
    bower install

### Testing

Tests are run using [web-component-tester](https://github.com/Polymer/web-component-tester):

    npm install -g web-component-tester
    wct

### Demonstration & Documentation

Demonstration and documentation are viewed using [polyserve](https://github.com/PolymerLabs/polyserve):

    npm install -g polyserve
    polyserve

