# Adding a script

MXML files insert ActionScript code through a `<s:Script>` tag containing code inside a `<![CDATA[ ... ]]>` markup.

```mxml
<?xml version="1.0"?>
<s:Page
    xmlns:s="http://www.steel.net/ver/1"
    path="/">
    <s:Script>
        // ActionScript code
    </s:Script>
</s:Page>
```

For initialiser code, handle the `creationComplete` event in the `s:Page` tag:

```mxml
<?xml version="1.0"?>
<s:Page
    xmlns:s="http://www.steel.net/ver/1"
    path="/"
    creationComplete="initialise()">
    <s:Script>
        private function initialise():void
        {
            trace("Hello world");
        }
    </s:Script>
</s:Page>
```