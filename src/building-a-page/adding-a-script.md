# Adding a script

MXML files insert ActionScript code through a `<ie:Script>` tag containing code inside a `<![CDATA[ ... ]]>` markup.

```mxml
<?xml version="1.0"?>
<ie:Page
    xmlns:ie="iron://engine.net/1.0"
    path="/">
    <ie:Script>
        <![CDATA[
        // ActionScript
        ]]>
    </ie:Script>
</ie:Page>
```

For initialiser code, handle the `creationComplete` event in the `s:Page` tag:

```mxml
<?xml version="1.0"?>
<ie:Page
    xmlns:ie="iron://engine.net/1.0"
    path="/"
    creationComplete="initialise()">
    <ie:Script>
        <![CDATA[
        private function initialise():void
        {
            trace("Hello world");
        }
        ]]>
    </ie:Script>
</ie:Page>
```