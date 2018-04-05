#Xpath

—

## Xpath

Xpath is used to traverse the elements of an XML document

—

## Xpath expression

- Uses path notation
- Will evaluate to a node-set, boolean, number, or string

—

[.build-lists: true]

## Syntax - Location Path

> A location path is an XPath expression used for selecting a set of nodes relative to the context node

- Relative path - selects nodes relative to it’s context
locationstep/locationstep/locationstep
- Absolute path - starts at the root element
/locationstep/locationstep/locationstep

—

## Syntax - Location Path

- Recursive descent
//rooms

—

[.build-lists: true]

## Syntax - Location Steps


```
axis::nodetest[predicate]
```

- axis - relationship between the context node and the nodes to be selected
- nodetest - the name of the node
- predicate - expression to refine the set of nodes selected by the location step

—

## Axes

[https://developer.mozilla.org/en-US/docs/Web/XPath/Axes](https://developer.mozilla.org/en-US/docs/Web/XPath/Axes)

—

## Nodetest

> The node test is the only required portion of an XPath location step

- The actual name of the node
- asterisk

—

## Predicates

—

![fill autoplay mute loop](../_images/gifs/thumbsup.mp4)

# Thanks!