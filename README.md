# ArrayForth Mode

This is a simple Emacs mode for editing arrayForth and colorForth files. This lets you use normal Forth syntax while presenting a colorForth style colored output. The output essentially follows the conventions outlined in [this][1] post. You can run the file through some automated script to get actual array/colorForth output.

[1]: http://www.strangegizmo.com/forth/ColorForth/msg00209.html

In the immediate future, I want to add support for making this transformation automatic. Additionally I am going to make the basic functionality more robust and add some commands specific to arrayForth.

## Installation

For now, you can install this mode by putting it somewhere on your load path. After that, add the following line to your `.emacs` file:

    (require 'array-forth-mode)
    
You can also set this as the default mode for editing `*.fs` files:

    (add-to-list 'auto-mode-alist '("\\.fs" . array-forth--mode))
