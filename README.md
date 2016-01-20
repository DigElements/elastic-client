##&lt;elastic-client&gt;

`elastic-client` is an element that makes a connection to an elasticsearch
server via the standard elasticsearch javascript api.  Once a connection is 
established, the client property can be used by other elements in the applications
to access the elastic REST api


Example:
```html
<elastic-client
config='{"host": "http://localhost:9200"}'
client={{esclient}}></elastic-client>

<search-es 
client="[[esclient]]"
index="myindex"
index-type="[[indexType]]"
query-results="{{results}}"></search-es>
```



