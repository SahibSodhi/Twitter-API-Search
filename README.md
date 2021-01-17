## Search for tweets using Twitter search/streaming api
Search for certain tweets using keywords specified in a mysql database using the search api, streaming api or both at the same time.
### Requirements other than codeigniter
* curl
* memcache/memcached (optional for caching)
* twitter account (optional for streaming api)

### How it works
1. Queries the db for specified keywords (can be 'string' or '#string' or '@string')
2. Two command line functions - search() and stream() let you choose whether to stream or search.

It is possible to run search() within the site but its a good idea to use its cache feature to avoid getting banned by twitter.

Search() is designed to be run with cron or directly on the site.
Stream() is best run with something like nohup as it is an endless loop.
