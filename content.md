# vendor api
In general the XWS team provides the XING API,
whoch is a public api and can be used by third parties to interact with XING data.
But for some cases, when api is relevant only for a small amount of consumers,
like our mobile tracking api, xws provide Vendor Proxy.
In this case teams develop api themselves and use the xws infrastructure.


# how to develop vendor API
### LINKS###

### iphone-app ####
to test mobile app

### errors ###

read xws guidelines

#### vendor api ###
for tracking goals is better, because no external calls should be allowed
authentication via Oauth (logged in) or API_KEY (logged out)

### public api ###
can be used by everybody
no authentication, rid used
put logic on our side

xws tam prepares "Packman" for maintaining api's

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


