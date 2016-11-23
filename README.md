##&lt;elastic-client&gt;

`elastic-client` is an element that makes a connection to an elasticsearch
server via the standard elasticsearch javascript api.  Once a connection is 
established, the client property can be used by other elements in your application
to access the elastic REST api


Example:
```html
<elastic-client
config='{"host": "http://localhost:9200"}'
client="{{esclient}}"></elastic-client>

<elastic-client-search
client="[[esclient]]"
index="myindex"
type="[[indexType]]"
body='{"query": {"match_all": {}}}'
results="{{results}}"
last-error="{{error}}">
</elastic-client-search>
```

## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install