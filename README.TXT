Time Travelers' Proxy
=====================
What is this?
-------------
This is a simple HTTP proxy to the WayBack machine and the Portuguese web archive (tries both).

How to use?
-----------
You will need bash and coreutils.
Note that you will need your own TCP server.
1.	Change configure.sh to your likeing
2.	Start your favorite TCP server, executing script ``httpd'' on connection.
	a)	`busybox nc -ll -p 8080 -e sh -c './httpd'`
	b)	`ncat -lkp 8080 -c './httpd'`
3.	Point your browser's HTTP proxy settings to your server.
4.	Point your browser to `http://altavista.digital.com/`, enter your query, and search the web!
5.	Point your browser to `http://[YOURIP]:[YOURPORT]/` to browse server files.
6.	Point your broswer to `http://www.msn.com/tutorial/default.html` for an Internet tutorial.

Considerations
--------------
The Time Travelers' Proxy is intended to be used for late 1990s web surfing.
Web search functionality is very limited. The only search engine available trough this proxy is 1990s era AltaVista. 
This proxy is caching.
These scripts are buggy, slow, and dangerous. 

TODOs
-----
I'll probably get to these, eventually.
-	Fix various bugs.
-	Add more search engines.
-	Produce a NNTP proxy to Google Groups or the like.

Files
-----
README.TXT	This file
httpd	Simple HTTP Server
proxy.sh	Processes proxy requests through the numbered files in order
archive.sh	Provides functions for archive grabbing
configure.sh	Configuration file
error.sh	Generates two types of error pages
fonts.sh	Provides fancy terminal text
search.sh	Proves basic search functionality
wecache.sh	Wget, but with cache
0.dium.sh	Deals with the ``dium.htm'' links generated by the Portuguese web archive
10.index.sh	Process local file requests
50.general.sh	Random rules
100.default.sh	Default rule to process web requests
110.live.sh	Maybe the website is live?


