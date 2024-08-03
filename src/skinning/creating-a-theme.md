# Creating a theme

A theme defines a cascading style sheet that may be applied to the Iron application.

A theme is logical, therefore it is an AS file defining a class that extends iron.skins.Theme.

```as3
package
{
    import iron.skins.*;

    public class HelloWorldTheme extends Theme
    {
    }
}
```

## Linking a cascading style sheet file

A theme may link a cascading style sheet file for expressing the user interface skins in a concise way.

- The `PropertyReference(name)` CSS calls resolve to a property within the iron.skins.Theme subclass scope, whether it is a static property or an instance property.

```as3
package
{
    import iron.skins.*;

    [SkinSheet(source="style.css")]
    public class HelloWorldTheme extends Theme
    {
    }
}
```

Example cascading style sheet:

```css
@namespace s "iron://engine.net/1.0";

@font-face {
    fontFamily: "Open Sans";
    fontWeight: 100 700;
    fontStyle: normal;
    src: url("opensans.ttf");
}

s|Button {
    fontFamily: "Open Sans";
}
```