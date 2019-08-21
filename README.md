[![Melpa Status](http://melpa.org/packages/ns-auto-titlebar-badge.svg)](http://melpa.org/#/ns-auto-titlebar)
[![Melpa Stable Status](http://stable.melpa.org/packages/ns-auto-titlebar-badge.svg)](http://stable.melpa.org/#/ns-auto-titlebar)
<a href="https://www.patreon.com/sanityinc"><img alt="Support me" src="https://img.shields.io/badge/Support%20Me-%F0%9F%92%97-ff69b4.svg"></a>

ns-auto-titlebar.el
===================

Recent builds of Emacs (27, 26?) support transparent titlebars on
MacOS via the `ns-transparent-titlebar` and `ns-appearance` frame
properties. The latter indicates whether the titlebar background
should be `dark` or `light`, and it is not set automatically by
Emacs. However, the text colour is always taken from the current
theme, which can lead to unreadable titlebar text if `ns-appearance`
is not set correctly.

This Emacs package provides a global minor mode,
`ns-auto-titlebar-mode` which - when enabled - keeps the
"ns-appearance" frame parameter correctly set in GUI frames so that it
matches the currently-enabled theme, whether it is light or dark.

For this package to work correctly, it is generally necessary that the
theme you use sets the `frame-background-mode` variable appropriately.
This can be set manually if necessary, but see the docs for that
variable.

Installation
=============

If you choose not to use one of the convenient
packages in [MELPA][melpa], you'll need to
add the directory containing `ns-auto-titlebar.el` to your `load-path`, and
then `(require 'ns-auto-titlebar)`.

Usage
=====

Enable `ns-auto-titlebar-mode` with `M-x customize`, or like this:

```elisp
(when (eq system-type 'darwin) (ns-auto-titlebar-mode))
```
Note that it is safe to omit the "when" condition if you prefer.

[melpa]: http://melpa.org

<hr>


[💝 Support this project and my other Open Source work](https://www.patreon.com/sanityinc)

[💼 LinkedIn profile](https://uk.linkedin.com/in/stevepurcell)

[✍ sanityinc.com](http://www.sanityinc.com/)

[🐦 @sanityinc](https://twitter.com/sanityinc)
