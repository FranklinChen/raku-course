---
title: loop
---

{% include menu.html %}

The `loop` statement is a construct in Raku that has a lot of common with traditional loops in the C programming language and its relatives. It takes three statements: the initialiser, the test, and the statement to modify the loop variable. The body of the loop is repeatedly executed while the test remains `True`.

```raku
loop (my $c = 0; $c < 5; $c++) {
    say "The current value of the counter is $c.";
}
```

Here, `++` is a postfix operator that increments its argument by 1. We will cover more operators in the second part of the course.

The program executes the body of the loop five times.

```console
$ raku t.raku
The current value of the counter is 0.
The current value of the counter is 1.
The current value of the counter is 2.
The current value of the counter is 3.
The current value of the counter is 4.
```

Some, or even all, of the statements in `loop`’s header may be omitted. For instance, here is the same program:

```raku
my $c = 0;
loop (; $c < 5;) {
    say "The current value of the counter is $c.";
    $c++;
}
```

## * * *

The `loop` loops are, probably, the least used loops in Raku. They can be found, for example, in an automated translator from C to Raku. In Raku, though, there are handier loops such as `for`, which we are examining very soon.

{% include nav.html %}
