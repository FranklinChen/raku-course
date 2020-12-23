---
title: Multi-line comments
---

[Start](/raku-course/) / [Part 1](/raku-course/part1) / [Comments](/raku-course/comments)

# Multi-line comments

As soon as you want to leave a comment that is more than a single line, you can choose either to have a few single-line comments or a single multi-line comment.

Multi-line comments start with a two-character combination ``#` `` and are followed by a pair of enclosing characters `( )`, `{ }`, `[ ]`, or `< >` or their paird multiple copies: `(( ))`, `[[[ ]]]`, etc.

For example:

    my $name;
    #`( We are going to ask the user
    to enter their name first and then
    save the input in a variable. )

    $name = prompt 'What is your name? ';
    #`{ The program now waits
    until the user enters the name
    and presses Enter. }

    say $name; #`( And now we can print it )

## Course navigation

← [Comments](/raku-course/comments) / [Single-line comments](/raku-course/comments/single-line) | [Comments](/raku-course/comments) / [Embedded comments](/raku-course/comments/embedded)  →