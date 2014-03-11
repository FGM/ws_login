ws_login
========

A login module for web service authentication: expose Drupal login to REST-ish clients

Logging in
----------

Send a HTTP POST request to the site:

- URL: ws_login/login
- Content-type: application/json
- Content:
  {
    "name": "some user name",
    "pass": "some password"
  }

Only not-logged-in users may log in.


Logging out
-----------

Send a HTTP GET to the site:
- URL: ws_login/logout

Only logged-in users may log out.
