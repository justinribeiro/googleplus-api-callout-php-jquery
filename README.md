Pulling data from Google Plus streams with PHP and displaying with jQuery
=================================

The following example pulls data from the Google API for Google+ via PHP, stores the data in cache file (which is checked on an interval of 10 minutes), and 
then is muxed with a jQuery ajax converter to inject into a jsRender template.

Things you need to make this work
===
<ol>
	<li>Google API key (https://code.google.com/apis/console/)</li>
	<li>Google+ User ID (the working example uses my id)</li>
	<li>Write access to whereever me.json gets written</li>
</ol>

Things to note
===
<ol>
	<li>You don't have to use jsRender (it's overkill for this simple example, but I was previsouly testing something else so I left it). Note this is the OLD version of JsRender; the new version has a different template format.</li>
	<li>Similarly, you don't have to use the ajax converter (you could very well do that server side or change the API call query). Again, I was testing something else, so it stuck around.</li>
	<li>The Google API for Google+ has a courtesy limit of 1,000 queries per day, hence the json cache file.</li>
	<li>You could very well write the exact same cache script in Node.js, Ruby, Python, Perl, whatever. There's nothing inherently special about the PHP.</li>
	<li>The API query really only looks for type "article" for shared links; you can pretty much pull back anything you want. I just used this as a simple example case.</li>
	<li>This doesn't use the Google Plus PHP helper (http://code.google.com/p/google-plus-php-starter/), which wasn't out when I wrote this example.</li>
</ol>

Working Example
===
http://stickmanventures.com/labs/demo/googleplus-api-callout-php-jquery/

Blog blog blog
===
The small write up about it via the <a href="http://blog.stickmanventures.com/2011/11/16/pulling-data-from-google-stream-caching-with-php-and-displaying-with-jquery/">SV blog</a>.