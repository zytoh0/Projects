Captcha
================

Captcha is an optical character recognition (OCR) tool for Captchas.
That is, it will recognize and "read" the text embedded in images and write the recognized text to a file.

USAGE
-----
The following code block only work in Captcha.ipynb

.. code-block:: python

    Captcha(im_path, save_path);
    """
    im_path: .jpg image path to load and to infer
    save_path: output file path to save the one-line outcome
    """

.. code-block:: python

    import matplotlib.pyplot as plt, cv2, pytesseract

    # Simple image to txt file
    Captcha('./sampleCaptchas/input/input00.jpg', './sampleCaptchas/test.txt');

INSTALLATION
------------

Prerequisites:

- Captcha requires Python 3.6+
- You will need `Python Tesseract <https://pypi.org/project/pytesseract/>`_.
- You will need `OpenCV for Python <https://pypi.org/project/opencv-python/>`_.
- You will need the Python Imaging Library (PIL) (or the `Pillow <https://pypi.org/project/Pillow/>`_ fork).
  Under Debian/Ubuntu, this is the package **python-imaging** or **python3-imaging**.


CONTRIBUTOR
------------
- Originally written by `Zhi Yuan Toh <https://github.com/zytoh0>`_