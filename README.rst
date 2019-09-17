

indian name_match
==========

Indian Fuzzy Name matching like no other current algorithim.
Improvised verion of Soundex for Indian Name Matching.
Deals With:
-  Phonetic Variations  such as Pradeip Singh matches with Pradeep Singh.
-  Typographical Mistakes such as Mr Akhil Kumar matches with Akhil Kumar.
-  Reordered Items	Akhil Kumar and M/r Kumar Akhil will be a match.
-  Prefixes and Suffixex Siddhesh Sharma and s Sharma will be a match
-  Abbrevations and Initials Mr/miss etc all are preprocessed

I first preprocessed data also considering phonetic similarity of alphabets based on some common problems of Indian names.
After that i implemented soundex and used it to find similarity of names.
If two names seems similar , I have implmented my improvised vowels/cosonants functions which clears the situation better and gives an improvised Output.

Requirements
============

-  Python 3 or higher and nltk

Installation
============

Using PIP via PyPI

.. code:: bash

    pip3 install indian_namematch

or the following to install `python-Levenshtein` too

.. code:: bash

    pip install indian_namematch



Usage
=====

.. code:: python

    >>> import indian_namematch
    >>> from indian_namematch import fuzzymatch

Single Comparison
~~~~~~~~~~~~

.. code:: python

    >>> fuzzymatch.single_compare("A Singh", "Ajeet Singh")
        Match
    >>> fuzzymatch.single_compare("Ajeit Singh", "Ajeet Singh")
        Match
    >>> fuzzymatch.single_compare("Mr Ajeit Singh", "Ajeet Singh")
        Match
    >>> fuzzymatch.single_compare("M/r Ajeit Singh", "Ajeet Singh")
