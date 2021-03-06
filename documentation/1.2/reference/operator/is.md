---
layout: reference12
title_md: '`is` operator'
tab: documentation
unique_id: docspage
author: Tom Bentley
doc_root: ../../..
---

# #{page.title_md}

The non-associating, binary infix `is` operator is used to test the type of an 
expression.

## Usage 

<!-- try: -->
    void m(Object? obj) {
        Boolean isNumber = obj is Number<out Anything>;
        Boolean isNull = obj is Null;
    }

## Description

### Definition

The `is` operator is primitive.

Note that because Ceylon supports reified generics you may use `is` with a
parameterized type, for example you can write

<!-- try: -->
    Boolean intList = obj is List<Integer>;

### Polymorphism

The `is` operator is not [polymorphic](#{page.doc_root}/tour/language-module/#operator_polymorphism). 

### Type

The result type of the `is` operator is [`Boolean`](#{site.urls.apidoc_1_2}/Boolean.type.html).

### Note

Do not to confuse the `is` *operator* described here and which 
takes the infix form `attribute is Type` with the
[`is` *condition*](../../statement/conditions) used in `if`, `assert` and 
`while` statements and which takes the prefix form 
`is Type attribute`.

## See also

* [`extends` operator](../extends)
* [`satisfies` operator](../satisfies)
* [operator precedence](#{site.urls.spec_current}#operatorprecedence) in the 
  language specification
* [`if (is ...)` special form](../../statement/if#special_conditions)
* [`case (is ...)` special form](../../statement/switch#polymorphism)
