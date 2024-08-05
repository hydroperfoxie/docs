# Adding a script

MXML files insert ActionScript code through a `<i:Script>` tag containing code inside a `<![CDATA[ ... ]]>` markup.

```mxml
<?xml version="1.0"?>
<i:Page xmlns:i="iron://engine.1.0" path="/">
    <i:Script><![CDATA[
        // ActionScript
    ]]></i:Script>
</i:Page>
```

For initialiser code, handle the `creationComplete` event in the `s:Page` tag:

```mxml
<?xml version="1.0"?>
<i:Page xmlns:i="iron://engine.1.0" path="/" creationComplete="initialise()">
    <i:Script><![CDATA[
        private function initialise():void
        {
            trace("Hello world");
        }
    ]]></i:Script>
</i:Page>
```