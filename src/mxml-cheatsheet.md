# MXML cheatsheet

## Importing the engine namespace

```
xmlns:s="http://skyflex.com/1.0"
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
<s:xhtml>
    <h1>Title</h1>
    <p>Paragraph <b>number</b> <i>1</i></p>
    <ul>
        <li>Item a.</li>
        <li>Item b. {password.text}</li>
    </ul>
</s:xhtml>
```

## Inserting HTML

```mxml
<s:html value="{htmlSource.value}"/>
```