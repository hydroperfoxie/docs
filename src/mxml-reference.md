# MXML reference

MXML is an eXtensible Markup Language used for expressing user interface components over the ActionScript language.

## MXML file

A MXML file shall have a filename that identifies the name of the ActionScript class that it defines, while the parent directories after a source path determine the ActionScript package it belongs to.

Given that the SkyFlex manifest defines `source[0].path` as `"src"`, the following is an example MXML file defining the class `com.company.max.WeatherScreen`:

```mxml
<!-- src/com/company/max/WeatherScreen.mxml -->
<?xml version="1.0"?>
<s:HGroup xmlns:s="http://skyflex.com/1.0">
    <s:Label variant="heading" value="Weather"/>
</s:HGroup>
```

## i prefix

The convention is to assign the `i` prefix as the URI `http://skyflex.com/1.0`, identifying the SkyFlex elements and component set.

## &lt;i:Script/&gt;

The `<s:Script/>` element is used for defining properties and methods inside the component using the ActionScript language.

```mxml
<?xml version="1.0"?>
<s:HGroup xmlns:s="http://skyflex.com/1.0">
    <s:Script><![CDATA[
        // definitions
    ]]></s:Script>
</s:HGroup>
```