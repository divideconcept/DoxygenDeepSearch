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
Append <script id="searchdata" type="text/xmldata"> to the content of html/search.html, then paste the content of searchdata.xml, and end with </script>.
Replace html/search/search.js by Doxygen Deep Search search.js.

That's it !

If you need to automate this in a script:

### BATCH

copy /y search.js html/search/search.js  
echo ^<script id='searchdata' type='text/xmldata'^> >> html/search.html  
type searchdata.xml >> html/search.html  
echo ^</script^> >> html/search.html

### BASH

cp search.js html/search/search.js  
echo \"<script id=\'searchdata\' type=\'text/xmldata\'>\" >> html/search.html  
cat searchdata.xml >> html/search.html  
echo \"</script>\" >> html/search.html
