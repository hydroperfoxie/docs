# Getting started

Pages are MXML files containing a `<i:Page>` tag that explicitly sets the path rule.

Here is an example:

```mxml
<!-- src/com/example/pages/Home.mxml -->
<?xml version="1.0"?>
<i:Page xmlns:i="iron://engine.1.0" path="/">
    <i:Label text="Hello world!"/>
</i:Page>
```