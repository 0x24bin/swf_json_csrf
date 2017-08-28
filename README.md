## Purpose
This repository was created to simplify the SWF-based JSON CSRF exploitation (in the future commits i will also add custom Content-Type header support, so you should be able to send other data types, like XML).

## Instructions
The .swf file take 4 parameters:
1) **jsonData** - apparently, JSON Data:)
2) **php_url** - URL of the 307 redirector php file.
3) **endpoint** - target endpoint, which is vulnerable to CSRF.
4) **ct** (optional) - specify your own Content-Type. Without this parameter it will be `application/json`

Place test.swf, test.php and crossdomain.xml on your host, then simply call the SWF file with the correct parameters.

Example call:
https://yourhost.com/test.swf?jsonData={"test":1}&php_url=https://yourhost.com/test.php&endpoint=https://targethost.com/endpoint


## Thanks
Special thanks to the https://twitter.com/emgeekboy, who inspired me to make this repository.
Related blog posts about this: 
* http://www.geekboy.ninja/blog/exploiting-json-cross-site-request-forgery-csrf-using-flash/
* http://research.rootme.in/forging-content-type-header-with-flash/
* http://resources.infosecinstitute.com/bypassing-csrf-protections-fun-profit/#gref

## Commits, PRs and bug reports are welcome!
