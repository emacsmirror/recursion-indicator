# recursion-indicator.el - Recursion level indicator in the mode-line

![recursion-indicator](https://github.com/minad/recursion-indicator/blob/master/recursion-indicator.png?raw=true)

This simple library shows the current recursion level in the mode-line.
For example if you `enable-recursive-minibuffers` and enter `M-x recursive-edit M-x recursive-edit M-x M-x M-x`,
the modeline indicator will show `[↲↲↲⟲⟲]`. This indicator is an alternative
to the brackets, Emacs shows by default around the modes, and to the counter shown
if `minibuffer-depth-indicate-mode` is activated.

If you are using `recursion-indicator` you might want to remove `%[` and `%]` from `mode-line-modes`
and disable `minibuffer-depth-indicate-mode`.

## Usage

~~~ elisp
(use-package recursion-indicator
  :demand t
  :config
  (recursion-indicator-mode))
~~~