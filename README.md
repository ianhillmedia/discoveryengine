# discoveryengine
A basic content discovery engine.

Working from https://developers.google.com/custom-search/json-api/v1/using_rest

And http://stackoverflow.com/questions/22223146/is-there-a-working-sample-of-the-google-custom-search-rest-api


Login to Google

Go to https://cse.google.com/cse/all

Create a New Search Engine

Add any URL (You'll remove it later to do a search of the entire web)

Click Create

Now reopen your Search Engine

Under Basics, scroll to Sites to search. Select the site you added and Delete it 

Scroll to Restrict Pages using Schema.org types. Add up to 10 Schema.org types to restrict your search results. Schema types will auto-fill. See http://schema.org/docs/full.html

(Do you have to click update at the bottom of the page?)



Look at the URL for your Search Engine. It will look something like https://cse.google.com/cse/setup/basic?cx=009154861957663122999:ftxh8pb_zhu

Copy your cx from the URL

In a new tab, go to https://console.developers.google.com/apis/library?project=millennial-mobile-moms-search

Search for a Custom Search API

Click Custom Search API

Click Credentials > Create Credentials > API Key

Copy your API Key


In engine.html, look at your script src:

https://www.googleapis.com/customsearch/v1?key=APIKEYHERE&cx=CUSTOMSEARCHCXHERE&q=moms&dateRestrict=d[7]&fileType=HTML&callback=hndlr

Paste your API Key where it says APIKEYHERE and your cx where it says CUSTOMSEARCHCXHERE

Add search params using https://developers.google.com/custom-search/json-api/v1/reference/cse/list

Your script src should end with &callback=hndlr
