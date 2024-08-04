# MXML cheatsheet

## Importing the engine namespace

```
xmlns:ie="iron://engine.1.0"
```

## Importing an ActionScript package as a XML namespace

```
xmlns:xy="com.x.y.*"
```

Recursive:

```
xmlns:xy="com.x.y.**"
```

## Data binding

```
text="Last password: {password.text}"
```

## Handling an event

```
click="trace('click event:', event);"
```

## Inserting XHTML

```mxml
<ie:xhtml>
    <h1>Title</h1>
    <p>Paragraph <b>number</b> <i>1</i></p>
    <ul>
        <li>Item a.</li>
        <li>Item b. {password.text}</li>
    </ul>
</ie:xhtml>
```

## Inserting HTML

```mxml
<ie:html value="{htmlSource.value}"/>
```