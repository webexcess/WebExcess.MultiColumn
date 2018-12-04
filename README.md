# WebExcess.MultiColumn Package for Neos CMS #
[![Latest Stable Version](https://poser.pugx.org/webexcess/multicolumn/v/stable)](https://packagist.org/packages/webexcess/multicolumn)
[![License](https://poser.pugx.org/webexcess/multicolumn/license)](https://packagist.org/packages/webexcess/multicolumn)

Bootstrap grid for Neos CMS

![WebExcess.MultiColumn](Documentation/preview.gif "WebExcess.MultiColumn")

## Compatibility and Maintenance
WebExcess.MultiColumn is currently being maintained for Neos 2.3 LTS and Neos 3.x.

| Neos Version | WebExcess.MultiColumn Version | Maintained |
|--------------|-------------------------------|------------|
| Neos 4.x     | 3.x                           | YES        |
| Neos 3.x     | 2.x                           | NO         |
| Neos 2.3 LTS | 1.x                           | NO         |

## Installation
```
composer require webexcess/multicolumn
```

## Configuration

### Restricted content

To allow your content elements to be inserted in a column, you have to add the following to your NodeType:

```
Your.Package:NodeType:
  superTypes:
    WebExcess.MultiColumn:Constraint.Column.Allowed: true
```

### Row dialog

When inserting a row, 2 columns are inserted by default. To improve the user experience, the `WebExcess.MultiColumn:Mixin.Row.Dialog` can be added. This will ask for the number of columns when inserting.

```
WebExcess.MultiColumn:Row:
  superTypes:
    WebExcess.MultiColumn:Mixin.Row.Dialog: true
```

### Disable property

To disable e.g. the offset, override in your package the column NodeType by the following:

```
WebExcess.MultiColumn:Column:
  superTypes:
    WebExcess.MultiColumn:Mixin.Column.Offset: false
```

To disable e.g. only the xl property, you can just disable the `WebExcess.MultiColumn:Mixin.Column.Offset.XL` mixin.

```
WebExcess.MultiColumn:Column:
  superTypes:
    WebExcess.MultiColumn:Mixin.Column.Offset.XL: false
```
