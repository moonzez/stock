# vendor api
XWS team provides the XING API,
which is a public api and can be used by third parties to interact with XING data.
But for some cases, when api is relevant only for a small amount of consumers,
like our mobile tracking api, xws provide Vendor Proxy.
In this case teams develop api themselves and use the xws infrastructure.
Rough process:
* call vendor proxy resource
* Verify namespace, if it exists
* Authentication (Oauth and API_KEY for logged out)
* check permissions for consumer
* Call the Vendor API
* Respond with status code and response body


# how to develop vendor API
## add new configurations to xws project  (TODO) link to config on xws master
## In order to access the Vendor API, an API consumer must have the required permission. Contact xws team to get permissions
## write vendor api
## write documentation

### TODO: link to how to develop

# Good to know
## The XING API uses "scrambled IDs". It is normal user id + checksum. "1234_abcdef"
## Use versioning
with url is prefered by xws team, but with header is ok too.

#OAuth Curl Scripts
To test vendor API logged in user is needed. To simplify it, there is a
gem oauth-curl-scripts. It's a bash scripts generates Oauth parameters for call and allow us to add own calls to our vendor api. Currently only for mobile vendor api TODO link!

### iphone-app #
to test mobile app

### errors ###

read xws guidelines


### curl oauth gem ####
to test public/vendor api use curl script to execute calls
take consumer data
sandbox/v1/admin
generate tocken with xAuth
paste in _config.rb

### versioning ###
with url is prefered by xws team, but with header is ok too.

### xing-xws_pilot ###
test tool


xws/engines...events/
resource-load /endpoint

### documentation in developers portal
