Running a Search
----------------
To search the database we're built, you just run our simple search engine:

.. xapianrunexample:: search1
    :args: db watch

These results show that 7 documents match our search for the term
'watch', providing the document IDs (e.g. #004) and title for each.
If you want to search for multiple words, just chain them together on
the command line:

.. xapianrunexample:: search1
    :args: db Dent watch

You'll notice that all of the results from the first time come back
the second time also, with additional ones (the match 'Dent' but not
'watch'), because by default QueryParser will use the OR operator to
combine the different search terms. Also, because #046 contains both
'Dent' and 'watch', it now ranks highest of all the matches.
