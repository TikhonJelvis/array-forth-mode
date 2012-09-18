# ArrayForth Mode

This is a simple Emacs mode for editing arrayForth and colorForth files. This lets you use normal Forth syntax while presenting a colorForth style colored output. The output essentially follows the conventions outlined in [this][1] post. You can run the file through some automated script to get actual array/colorForth output.

[1]: http://www.strangegizmo.com/forth/ColorForth/msg00209.html

In the immediate future, I want to add support for making this transformation automatic. Additionally I am going to make the basic functionality more robust and add some commands specific to arrayForth.

## Installation

This requires Emacs 24. Using it on Emacs 23 fails miserably (with a segfault!), so don't do it. 

For now, you can install this mode by putting it somewhere on your load path. After that, add the following line to your `.emacs` file:

    (require 'array-forth-mode)
    
You can also set this as the default mode for editing `*.cfs` files:

    (add-to-list 'auto-mode-alist '("\\.cfs" . array-forth-mode))
    
## Customization

You can control the actual colors of the various grammatical constructs. Each face is named after the color it gets in the normal arrayForth editor: for example, the face for definitions is called `array-forth-red-face`. You can modify these directly in your code by adding a line like

    (set-face-attribute 'array-forth-yellow-face nil :foreground "blue")

This changes the `array-forth-yellow-face` to have a blue color everywhere. 

You can also customize these faces with `M-x customize-group` followed by `array-forth-faces`. 
