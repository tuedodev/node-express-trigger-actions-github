# Node Express Server triggering a repository dispatch on Github actions

An intermediate Node Express Server between Sanity.io and Github actions in order to redeploy website after changes inside Sanity.io.

Roughly speaking, Sanity.io is sending a webhook via POST request to this Node Express Server, that can live on hosts like Heroku or Netlify. The express server in turn triggers a repository dispatch from outside in order to redeploy a website from Github to a remote server.
This intermediate server is necessary, because until now you cannot send an additional github token from Sanity.io.
