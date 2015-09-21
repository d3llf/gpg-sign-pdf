# gpg-sign-pdf
Embeed GPG signatures do PDF files
--------------

This is simple hack to embeed GPG clear signature to PDF file.

Such signed PDF files can be easily verified by *$gpg --verify file.pgp.asc.pdf*


## How this works?

gpg --clearsign substitutes "\n-" with "\n- -", which mess content
quite often. Sometimes it's better to substitute "\n-" patterns with
something different before clearsign kicks-in. This simple script substitutes
such patterns before clearsigning

Please be aware, that this can mess-up contents of your PDF, so try
different substitution pattern by flipping bits, and checking if your
PDF is still readable, or try to adapt your document before signing.
Usually this pattern is used to mark default color of text, so try to
change style of "Default" font from "Automatic" to "Black".

                                                      d3llf
