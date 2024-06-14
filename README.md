# Dude, Where's my JWT?
It can be really hard to know what the payload of an OIDC Identity Token is when sending to an IDP for exchange for a
bearer token.  I created a small tool to POST the base64 encoded JWT to an ephemeral webhook.  You can then copy the 
encoded JWT to see what the ID Token payload looks like.  This is useful for customizing the Claims that are present on the JWT

# How do I use this?
1. Fork this repo
1. Setup a new webhook at Webhook.site
1. Add that as a Github Actions repository variable called `WEBOOK_URL`
1. Run the workflow.  It's currently set to trigger manually or pushes to `main`
1. Go to the Webbook.site UI and grab the base64 encoded payload and paste it into the JWT decorder at JWT.io
1. View the payload of the JWT that Github is generating.

## Enjoy!