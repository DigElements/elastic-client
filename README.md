# elastic-client

A Polymer Element which creates and returns a client connection to an Elasticsearch server via the standard elasticsearch javascript API.  Once a connection is established, the client property can be used by other elements in your application to access the elastic REST API.

### Example
```html
<elastic-client
  config='{"host": "http://localhost:9200"}'
  client="{{esclient}}">
</elastic-client>

<elastic-client-search
  client="[[esclient]]"
  index="myindex"
  type="[[indexType]]"
  body='{"query": {"match_all": {}}}'
  results="{{results}}"
  last-error="{{error}}">
</elastic-client-search>
```

### Dependencies

Dependencies are installed using [Bower](http://bower.io/):

    npm install -g bower
    bower install

### Testing

Tests require a local instance of elasticsearch.

Tests are run using [web-component-tester](https://github.com/Polymer/web-component-tester):

    npm install -g web-component-tester
    wct

### Demonstration & Documentation

Demonstration and documentation are viewed using [polyserve](https://github.com/PolymerLabs/polyserve):

    npm install -g polyserve
    polyserve

