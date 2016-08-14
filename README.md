Doxygen Deep Search
===================

What it is
----------

The default Doxygen search engine only search for page titles and referenced code names, and it can't match partial names.  
The other Doxygen search engines only work server-side.  
Doxygen Deep Search is a replacement for the default search engine, it works both online and offline and search the whole text for occurences, even partial.

Install
-------

Generate your Doxygen project with the following HTML options enabled:  
SEARCHENGINE  
SERVER_BASED_SEARCH  
EXTERNAL_SEARCH

This will generate a searchdata.xml file.  
Append the content of that file at the end of html/search.html.  
Replace html/search/search.js by Doxygen Deep Search search.js.

That's it !
