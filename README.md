ws_login
========

A login module for web service authentication: expose Drupal login to REST-ish clients. 

Authentication is valid for normal web use and vice-versa. The main use case is probably 
in combination with the Drupal RestWS module ( https://drupal.org/project/restws ), since
it provides a login-controlled access to the RestWS URLs.

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
- Return: 200 on success, 401 + Authenticate header on failure

Only not-logged-in users may log in.


Logging out
-----------

Send a HTTP GET to the site:
- URL: ws_login/logout
- Return: 205 on success, 403 on failure

Only logged-in users may log out.
