# Creating a theme

A theme defines a cascading style sheet that may be applied to the Iron application.

A theme is logical, therefore it is an AS file defining a class that extends iron.themes.Theme.

```as3
package
{
    import iron.themes.*;

    public class HelloWorldTheme extends Theme
    {
    }
}
```

## Linking a cascading style sheet file

A theme may link a cascading style sheet file for expressing the user interface skins in a concise way.

```as3
package
{
    import iron.themes.*;

    [Theme(file = "style.css")]
    public class HelloWorldTheme extends Theme
    {
    }
}
```

Example cascading style sheet:

```css
@namespace s "http://www.iron.net/ver/1";

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