# MXML reference

MXML is an eXtensible Markup Language used for expressing user interface components over the ActionScript language.

## MXML file

A MXML file shall have a filename that identifies the name of the ActionScript class that it defines, while the parent directories after a source path determine the ActionScript package it belongs to.

Given that the Iron manifest defines `source[0].path` as `"src"`, the following is an example MXML file defining the class `com.company.max.WeatherScreen`:

```mxml
<!-- src/com/company/max/WeatherScreen.mxml -->
<?xml version="1.0"?>
<i:HGroup xmlns:i="iron://engine.1.0">
    <i:Label variant="heading" value="Weather"/>
</i:HGroup>
```

## i prefix

The convention is to assign the `i` prefix as the URI `iron://engine.1.0`, identifying the Iron Engine elements and component set.

## &lt;i:Script/&gt;

The `<i:Script/>` element is used for defining properties and methods inside the component using the ActionScript language.

```mxml
<?xml version="1.0"?>
<i:HGroup xmlns:i="iron://engine.1.0">
    <i:Script><![CDATA[
        // definitions
    ]]></i:Script>
</i:HGroup>
```