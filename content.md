# vendor api
XWS team provides the XING API,
which is a public api and can be used by third parties to interact with XING data.
But for some cases, when api is relevant only for a small amount of consumers,
like our mobile tracking api, xws provide Vendor Proxy.
In this case teams develop api themselves and use the xws infrastructure.

Rough process, what happens when vendor proxy resource gets called:
* Verify namespace, if it exists
* Authentication (Oauth and API_KEY for logged out)
* check permissions for consumer
* Call the Vendor API
* Respond with status code and response body


# how to develop vendor API
* add configs for a new vendor api to xws project. TODO LINK.
In order to access the Vendor API, an API consumer must have the required permission
Same root will be used to go to the documentation
* write vendor api
* write documentation, each vendor api should document all available calls. Will be accessable on [XING developer portal](http://dev.xing.com/docs/vendor_resources)
  * add mime type
  * route
  * documentation controller. Format is in documentation: TODO LINK.
    Note required keys

# Good to know
* The XING API uses "scrambled IDs". It is normal user id + checksum. "1234_abcdef"
* Use versioning

#OAuth Curl Scripts
To test vendor API logged in user is needed. To simplify it, there is a
gem oauth-curl-scripts. It's a bash scripts which generates all Oauth parameters for api call and allow us to add own calls to our vendor api. Currently only for mobile vendor api TODO link!
how to use it is described here:
TODO LINK
copy temp config to config, get consumer token from sandbox/v1/admin
generate tocken with xAuth
paste in _config.rb

### iphone-app #
to test mobile app

### errors ###

read xws guidelines


### xing-xws_pilot ###
test tool


xws/engines...events/
resource-load /endpoint
