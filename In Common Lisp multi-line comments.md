In Common Lisp, multi-line comments are written using **`#|`** to start the comment block and **`|#`** to end it.

```lisp
#|
This is a multi-line comment.
It can span across multiple lines.
|#
(defun hello ()
  (format t "Hello, World!"))

```

### Nesting Multi-Line Comments

Unlike many other languages, Common Lisp supports **nested** multi-line comments. This makes it easy to comment out large blocks of code that already contain multi-line comments without syntax errors:

```lisp
#|
  Outer comment starts here.
  
  #| 
    Inner nested comment block.
  |#
  
  Outer comment continues here.
|#

```

### Other Common Commenting Conventions

* **`;` (Single-line comment):** Comments out the remainder of the current line.
* **`;;` (Two semicolons):** Standard convention for code commentary inside a function/form.
* **`;;;` (Three semicolons):** Standard convention for title/header comments describing a section or file.
* **`#+nil` or `#-t` (Form commenting):** A Common Lisp trick used to safely comment out an entire S-expression regardless of lines:

```lisp
#+nil
(this entire form is ignored by the reader)

```