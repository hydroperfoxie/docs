# MXML cheatsheet

## Importing the engine namespace

`xmlns:ie="http://www.iron.net/1.0"`

## Importing an ActionScript package as a XML namespace

`xmlns:xy="com.x.y.*"`

Recursive:

`xmlns:xy="com.x.y.**"`

## Data binding

`text="Last password: {password.text}"`

## Handling an event

`click="trace('click event:', event);"`

## Inserting HTML

```mxml
<ie:XH>
    <h1>Title</h1>
    <p>Paragraph <b>number</b> <i>1</i></p>
    <ul>
        <li>Item a.</li>
        <li>Item b. {password.text}</li>
    </ul>
</ie:XH>
```

Data binding expressions contribute plain text, not a HTML text. For that case, use or nest the following to use an expression that returns a HTML text that is displayed directly by the browser:

```mxml
<ie:XH value="{htmlSource.value}"/>
```