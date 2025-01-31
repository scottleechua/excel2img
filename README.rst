excel3img
=========

A functioning fork of the `excel2img <https://github.com/glexey/excel2img>`__ package by Alexey Gaydyukov.

Save ranges from Excel documents as images

Requirements
------------

1. Python 2.7, 3.3 or later
2. `pywin32 <http://sourceforge.net/projects/pywin32/files/pywin32>`__
3. `Pillow <https://pypi.python.org/pypi/Pillow>`__ >= 3.3.1
4. Microsoft Excel (tested with Office 2013, on Windows 10)

Installation
------------

.. code:: shell

    pip install excel3img

Usage as python module
----------------------

.. code:: python

    import excel3img

    # Save as PNG the range of used cells in test.xlsx on sheet named "Sheet-1"
    excel3img.export_img("test.xlsx", "test.png", "Sheet-1")

    # Save as BMP the range B2:C15 in C:Users\admin\test.xlsx on sheet named "Sheet2"
    excel3img.export_img(r"C:Users\admin\test.xlsx", "test.bmp", "Sheet2", "B2:C15")

    # Save as GIF the range "MyNamedRange" in test.xlsx
    excel3img.export_img("test.xlsx", "test.gif", "", "MyNamedRange")

Usage from command line
-----------------------

.. code:: shell

    # Save as PNG the range of used cells in test.xlsx on first sheet
    python excel3img.py test.xlsx test.png

    # Save as BMP the range A1:D4 in C:Users\admin\test.xlsx on sheet named "Sheet3"
    python excel3img.py "C:\Users\admin\test.xlsx" test.bmp -p Sheet3 -r A1:D4
    
    # Save as GIF the range "MyNamedRange" in test.xlsx
    python excel3img.py test.xlsx test.gif -r MyNamedRange

Author
=======

excel2img by Alexey Gaydyukov <glexey@gmail.com>

excel3img fork maintained by Scott Lee Chua <scottleechua@gmail.com>

License
========
Apache License 2.0

Credits
========
Inspired by `visio2img <https://github.com/visio2img/visio2img>`__

