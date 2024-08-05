# MXML reference

MXML is an eXtensible Markup Language used for expressing user interface components over the ActionScript language.

## MXML file

A MXML file shall have a filename that identifies the name of the ActionScript class that it defines, while the parent directories after a source path determine the ActionScript package it belongs to.

Given that the Iron manifest defines `source[0].path` as `"src"`, the following is an example MXML file defining the class `com.company.max.WeatherScreen`:

```mxml
<!-- src/com/company/max/WeatherScreen.mxml -->
<?xml version="1.0"?>
<ie:HGroup xmlns:ie="iron://engine.1.0">
    <ie:Label variant="heading" value="Weather"/>
</ie:HGroup>
```

## ie prefix

The convention is to assign the `ie` prefix as the URI `iron://engine.1.0`, identifying the Iron Engine elements and component set.

## &lt;ie:Script/&gt;

The `<ie:Script/>` element is used for defining properties and methods inside the component using the ActionScript language.

```mxml
<?xml version="1.0"?>
<ie:HGroup xmlns:ie="iron://engine.1.0">
    <ie:Script><![CDATA[
        // definitions
    ]]></ie:Script>
</ie:HGroup>
```