# Reflection

## What did I repeat by hand?

The `<header>`, `<nav>`, and `<footer>` are byte-for-byte identical on all nine
pages. I pasted that block nine times. Every time I touched the wordmark or a nav
label, I had to make the same edit in nine files and sometimes would miss some, which was annoying.

## What broke when I moved a file?

Paths. The four family pages and the guide index live in `guide/`, so every
stylesheet, image, and nav link there needs a `../` that the root pages don't.

## What would I want a tool to generate for me?

A layout/partial system: write the header, nav, footer, and the `<head>`
boilerplate **once**, and have every page include them with paths resolved
automatically for that page's depth. Give me one "current page" variable so the
nav can mark itself.

