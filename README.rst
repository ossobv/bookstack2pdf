BookStack2PDF
=============

Add the following to the book base ``description``::

    This text is not shown.
    Nor is this.

    <comment>See https://github.com/ossobv/bookstack2pdf</comment>
    <version>v1.1 (22-feb-2022)</version>
    <author>John Doe</author>
    <recipients>- v1.1 (recipientX, recipientY)</recipients>
    - v1.0 (recipientX)</recipients>

Then, export the `BookStack book <https://www.bookstackapp.com/>`_ book
as a **Contained Web File (.html)**.

Then, feed that export (``export-v1.1.html``) to this script::

    LANG=nl ./bookstack2pdf export-v1.1.html export-v1.1.pdf


Requirements
------------

A patched ``wkhtmltopdf`` is required, otherwise you'll get these errors::

    The switch --disable-external-links, is not support using unpatched
    qt, and will be ignored.
    The switch --footer-font-name, is not support using unpatched qt,
    and will be ignored.
    The switch --footer-font-size, is not support using unpatched qt,
    and will be ignored.
    The switch --footer-spacing, is not support using unpatched qt, and
    will be ignored.
    The switch --footer-left, is not support using unpatched qt, and
    will be ignored.
    The switch --footer-right, is not support using unpatched qt, and
    will be ignored.
    The switch --xsl-style-sheet, is not support using unpatched qt, and
    will be ignored.
    Error: This version of wkhtmltopdf is build against an unpatched
    version of QT, and does not support more then one input document.
    Exit with code 1, due to unknown error.

Precompiled binaries can be found at
`wkhtmltopdf downloads <https://wkhtmltopdf.org/downloads.html>`_.
