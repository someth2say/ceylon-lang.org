---
layout: reference13
title_md: '`-=` (subtract assign) operator'
tab: documentation
unique_id: docspage
author: Tom Bentley
doc_root: ../../..
---

# #{page.title_md}

The right-associative, binary infix `-=` operator decrements it's left-hand operand 
by the amount given by its right-hand operand. 

## Usage 

<!-- cat: void m() { -->
<!-- try: -->
    variable Integer num = 4;
    num -= 1; // decrement num by 1
    num -= num; // decrement num by 3
<!-- cat: } -->

## Description


### Definition 

The `-=` operator is defined as follows:

<!-- try: -->
    lhs = lhs.minus(rhs)

except that `lhs` is evaluated only once.

See the [language specification](#{site.urls.spec_current}#arithmetic) for more details.

### Polymorphism

The `-=` operator is [polymorphic](#{page.doc_root}/reference/operator/operator-polymorphism).
The definition of the `-=` operator depends 
on the [`Invertible`](#{site.urls.apidoc_1_3}/Invertible.type.html) interface.

### Type

The result type of the `-=` operator is the same as the type of its right hand operand.

## See also

* [arithmetic operators](#{site.urls.spec_current}#arithmetic) in the 
  language specification
* [operator precedence](#{site.urls.spec_current}#operatorprecedence) in the 
  language specification
* [Operator polymorphism](#{page.doc_root}/tour/language-module/#operator_polymorphism) 
  and 
  [Numeric operator semantics](#{page.doc_root}/tour/language-module/#numeric_operator_semantics) 
  in the Tour of Ceylon
