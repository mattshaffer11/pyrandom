=============
randpy
=============

.. image:: https://travis-ci.org/mattshaffer11/randpy.svg?branch=master
    :target: https://travis-ci.org/mattshaffer11/randpy
    :alt: Travis CI

.. image:: https://coveralls.io/repos/mattshaffer11/randpy/badge.svg?branch=master&service=github
    :target: https://coveralls.io/github/mattshaffer11/randpy?branch=master
    :alt: Coverage

randpy is a tiny set of utilities to generate random data such as strings, numbers, and dates.


Basic Data
---------------

.. code-block:: python

    >>> import randpy

    >>> randpy.random_boolean()
    True
    >>> randpy.random_boolean()
    False

    >>> randpy.random_integer(minimum=0, maximum=10)
    0
    >>> randpy.random_integer(minimum=0, maximum=10)
    10
    >>> randpy.random_integer(minimum=0, maximum=10)
    3

    >>> randpy.random_decimal(minimum=0, maximum=1)
    0.52
    >>> randpy.random_decimal(minimum=0, maximum=5, digits=4)
    1.9944

    >>> randpy.random_choice([1, 2, 3, 4])
    1

    >>> randpy.random_choices([1, 2, 3, 4], 2)
    [4, 4]
    >>> randpy.random_choices([1, 2, 3, 4], 3)
    [3, 1, 1]

Generators
---------------

.. code-block:: python

    >>> from randpy import generators

    >>> generators.phone_number()
    '2776904659'
    >>> generators.phone_number(international_code=True)
    '12776904659'

    >>> randpy.address()
    '865 Elm'
    >>> randpy.address()
    '652 S Blueridge Pl.'
    >>> randpy.address()
    '194 Country Ln.'

    >>> generators.email()
    'frank@aol.org'
    >>> generators.email()
    'kiara@aol.com'

    >>> generators.city()
    'Vancouver'
    >>> generators.city()
    'Chicago'

    >>> generators.state()
    'Rhode Island'
    >>> generators.state(abbrev=True)
    'RI'

    >>> generators.province()
    'Alberta'
    >>> generators.province(abbrev=True)
    'AB'

    >>> generators.lorem_ipsum()
    'Lorem ipsum dolor sit amet...'

    >>> generators.first_name()
    'Lucia'

    >>> generators.last_name()
    'Rossi'

    >>> generators.full_name()
    'Theo Santos'

    >>> generators.url()
    'https://www.wordpress.org'
