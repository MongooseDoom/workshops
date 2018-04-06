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
`locationstep/locationstep/locationstep`
- Absolute path - starts at the root node
`/locationstep/locationstep/locationstep`
- Double slash path - selects nodes anywhere in the tree 
`//rooms` would select all `rooms` nodes regardless of where they are nested within the XML

[.build-lists: true]

—

## Syntax - Location Steps


```
axis::nodetest[predicate]
```

- axis - relationship between the context node and the nodes to be selected
- nodetest - the name of the node
- predicate - expression to refine the set of nodes selected by the location step

—

## Axes are relationships

Axes have a direction of forward or reverse*
- ancestor*
- ancestor-or-self*
- attribute
- child
- descendant
- descendant-or-self
- following
- following-sibling
- parent
- preceding*
- preceding-sibling*
- self

![right 100%](http://courses.ischool.berkeley.edu/i290-14/s05/lecture-4/tree-relations.png)

[.autoscale: true]
[.footer: http://courses.ischool.berkeley.edu/i290-14/s05/lecture-4/allslides.html]

—

| Abbreviation | Equivalent with Axes |
| --- | --- |
| ../name | parent::name |
| name | child::name |
| //name | descendant::name |
| . | self::node() |
| * | child::* |
| @* | attribute::* |
| @name | attribute::name |

[.footer: http://courses.ischool.berkeley.edu/i290-14/s05/lecture-4/allslides.html]

—

## Axis examples in Raynor

```
<xsl:if test="child::page[not(@exclude='true')]"><xsl:text>parent </xsl:text></xsl:if>
```

the current context has children that do not use the exclude="true" attribute. Could this be written as `test="page[not(@exclude='true')]"`?

—
## Axis examples in Raynor

```
<xsl:if test="descendant-or-self::page[@id = //pageinfo/@id]"><xsl:text>current</xsl:text></xsl:if>
```

page node or a descendant of the page node has an id equal to the pageinfo id attribute

—

## Nodetest

> The node test is the only required portion of an XPath location step

- The actual name of the node or an asterisk
- The node that we are testing against
- Use @ for attributes

—

## Predicates []

> An expression enclosed in square brackets that results in a boolean value

- `//nav/page[1]` or `//nav/page[position()=1]` selects the first page node
- `//nav/page[last()]` selects the last page node
- `//nav/page[@id=56]` selects the last page with an id of 56
- `//nav/page[@id=//pageinfo/@id]` can have an whole other path within a prediate

—

## Chrome Extension

https://chrome.google.com/webstore/detail/xml-tree/gbammbheopgpmaagmckhpjbfgdfkpadb

—

![fill autoplay mute loop](../_images/gifs/thumbsup.mp4)

# Thanks!