---
title: Boolean operations with other types
---

{% include menu.html %}

In the next section, we will talk about converting data of different types to each other. But before that, it is important to highlight the following feature of Raku. When you apply Boolean operations to strings or integers, the values are not converted to Booleans, and the result is not a Boolean value either. Consider the following examples:

```raku
say 'Hello' && 'World'; # World
say 'Alpha' || 'Beta';  # Alpha
say 0 ^^ 42;            # 42
```

Let us read the rules 📖 [from the documentation](https://docs.raku.org/language/operators#Tight_AND_precedence):

* `&&` returns the first argument that evaluates to False in Boolean context, otherwise returns the last argument.
* `||` returns the first argument that evaluates to True in Boolean context, otherwise returns the last argument.
* `^^` returns the True argument if there is one (and only one). Returns the last argument if all arguments are False. Returns `Nil` when more than one argument is true.

Notice that we just met a ‘null’ value `Nil`.

{% include nav.html %}
