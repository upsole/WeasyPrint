---
layout: page
title: "WeasyPrint 0.11: floats, Acid2 and unprefixing"
---

WeasyPrint 0.11 is out.

It has not been long since 0.10, but the point of this release is to
finally merge the support for floats and clear that we have had for a
while in an experimental branch.

With this (and countless other bug fixes), WeasyPrint now passes the
Acid2 test! See the [details](/#acid2) or try it yourself:

```
weasyprint http://www.webstandards.org/files/acid2/test.html acid2.pdf
weasyprint http://www.webstandards.org/files/acid2/test.html acid2.png
```

And now for something completely different, the `image-rendering`, `transform`,
`transform-origin` and `size` properties are unprefixed.  The prefixed form
(eg. `-weasy-size`) is ignored but gives a specific warning.

You **will** need to change your stylesheets if you used any of these with a
prefix.

As usual, the details of less visible changes are in the
[changelog](https://github.com/Kozea/WeasyPrint/blob/master/CHANGES).