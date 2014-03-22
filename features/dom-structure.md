# DOM Structure
This document describes how to define DOM document structure.

## Element Definition
An *Element Definition* is: the percentage symbol `%` followed by the **tagname** [(Identifier)](tokens.md#identifier) then **modifiers** (below) then **whitespace**  [(Whitespace)](tokens.md#whitespace) and then a **block**.

```
%div { ... }
%modal-container { ... }
%list_data { ... }
```

### Modifiers
Modifiers are added after the tagname and before the whitespace.

  * **class** and **attribute** modifiers can be added in any order
  * :warning: only one **id** modifier can be added per element definition and right after the tagname
  * :warning: the *id* attribute cannot be specified with both **id** modifier `#value` and **attribute** modifier `[id=value]`

### Classes
Classes to be added when the element is created can be defined with [CSS Class Selector](http://www.w3.org/TR/CSS21/selector.html#class-html). A class is: the dot character `.` followed by the **class name** [(Identifier)](tokens.md#identifier).

  * :warning: a class can only added once

```
%div.modal { ... }
%div.modal.big.blue { ... }
```

### Id
The id modifier specifies the value of the id attribute of the element: the hashmark symbol `#` followed by the **value** [(Identifier)](tokens.md#identifier)

```
%div#login-form { ... }
%h1#first-heading { ... }
```

### Attribute
Attribute modifiers defines attributes on an element, they are similar to [Attribute Selectors](http://www.w3.org/TR/CSS21/selector.html#attribute-selectors) but there is just one operator: opening bracket `[` then **attribute name** [(Identifier)](tokens.md#identifier) then equal symbol `=` then **value** [(Value)](tokens.md#value) the closing bracket `]`.

There is a shorthand notiation `[checked]` which translates to `[checked=true]`.

```
%input[type=text][placeholder=E-mail] { ... }
%input[type=checkbox][checked] { ... }
```

## Nesting
Elements can be nestied inside other elements. They keep the order which is defined.

```
%div {
  ...
  %span {
    ...
  }
}
```
