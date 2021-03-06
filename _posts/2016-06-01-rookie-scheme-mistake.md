---
title: Rookie Scheme Mistake
date: 2016-06-01 09:45:28
categories: code
tags: code scheme lisp functional-programming
img: /assets/scheme-language-logo.gif
excerpt: "<code>; application: not a procedure;</code>"
---

![]({{ site.baseurl }}/assets/scheme-language-logo.gif){:alt="Rookie Scheme Mistake"}

I'm currently reading [Structure and Interpretation of Computer Programs]({% post_url 2015-05-25-the-next-10-books %}) and during the first minutes of trying my luck into `scheme` I faced the following error:

```log
; application: not a procedure;
;  expected a procedure that can be applied to arguments
;   given: 5
```
After googling for a while without success I've realized that my rookie mistake. Instead of using the <del>super friendly</del> [Polish Notation](http://www.cs.man.ac.uk/~p/cs212/fix.html), I was using the usual Infix notation.

I had this:

```scheme
(define (square n)
  (n * n)
)

(square 5)
```

When I should be doing this:

```scheme
(define (square n)
  (* n n)
)

(square 5)
```

Problem solved :D
