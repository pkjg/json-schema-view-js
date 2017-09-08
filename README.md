# JSON Schema View (Pure JavaScript)

> A pure JavaScript component for rendering JSON Schema in HTML.

JSON Schema is very verbose and hard to read in JSON. This component helps rendering a JSON Schema in a user readable format.

[Also available as an AngularJS directive](https://github.com/mohsen1/json-schema-view)



### Usage

Installation

```
# Install via bower
bower install json-schema-view-js --save

# Install via NPM
npm install json-schema-view-js --save
```

Then either use global `JSONSchemaView` constructor or require if you need to

```js
const schema = {type: 'string', title: 'Name'};

const view = new JSONSchemaView(schema);

document.body.appendChild(view.render());
```

### API

#### `JSONSchemaView(schema [, open ] [, options])`

##### `schema` (`Object`) - **required**
The JSON Schema object.
##### `open` (`Number`)
Default: `1`
This number indicates up to how many levels the rendered tree should expand. Set it to `0` to make the whole tree collapsed or set it to `Infinity` to expand the tree deeply
##### `options` ('Object')
An object containing other options for construction the view. These are possible options:
###### `theme` (`string`)
A theme defined in the CSS of this view. Possible values: `dark`. Note that the dark theme is just for making the text brighter so it looks good on dark backgrounds.
###### `showRefs` (`boolean`)
to show refs as is. By default, the refs aren't handled and an 'undefined' is rendered.

## Development
Install `gulp` and run `gulp serve` to start the server that serves the development version of the project.

#### Running tests

**Once:**
```shell
npm test
```

**Continues:**
```shell
gulp test
```

### License
[MIT](./LICENSE)
