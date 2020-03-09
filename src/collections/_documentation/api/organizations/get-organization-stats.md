---
# This file is automatically generated from the API using `sentry/api-docs/generator.py.`
# Do not manually edit this file.
{
  "api_path": "/api/0/organizations/{organization_slug}/stats/", 
  "authentication": "required", 
  "description": "Return a set of points representing a normalized timestamp and the\nnumber of events seen in the period.", 
  "example_request": "GET /api/0/organizations/the-interstellar-jurisdiction/stats/ HTTP/1.1\nHost: sentry.io\nAuthorization: Bearer <token>", 
  "example_response": "HTTP/1.1 200 OK\nContent-Length: 481\nX-XSS-Protection: 1; mode=block\nX-Content-Type-Options: nosniff\nContent-Language: en\nAccess-Control-Expose-Headers: X-Sentry-Error, Retry-After\nVary: Accept-Language, Cookie\nAccess-Control-Allow-Methods: GET, HEAD, OPTIONS\nAllow: GET, HEAD, OPTIONS\nAccess-Control-Allow-Origin: *\nAccess-Control-Allow-Headers: X-Sentry-Auth, X-Requested-With, Origin, Accept, Content-Type, Authentication, Authorization\nContent-Type: application/json\nX-Frame-Options: deny\n\n[\n  [\n    1583643600.0, \n    6798\n  ], \n  [\n    1583647200.0, \n    7294\n  ], \n  [\n    1583650800.0, \n    6581\n  ], \n  [\n    1583654400.0, \n    8717\n  ], \n  [\n    1583658000.0, \n    6836\n  ], \n  [\n    1583661600.0, \n    7565\n  ], \n  [\n    1583665200.0, \n    4889\n  ], \n  [\n    1583668800.0, \n    6191\n  ], \n  [\n    1583672400.0, \n    8726\n  ], \n  [\n    1583676000.0, \n    7841\n  ], \n  [\n    1583679600.0, \n    7356\n  ], \n  [\n    1583683200.0, \n    7243\n  ], \n  [\n    1583686800.0, \n    6304\n  ], \n  [\n    1583690400.0, \n    6232\n  ], \n  [\n    1583694000.0, \n    7284\n  ], \n  [\n    1583697600.0, \n    5626\n  ], \n  [\n    1583701200.0, \n    6564\n  ], \n  [\n    1583704800.0, \n    5732\n  ], \n  [\n    1583708400.0, \n    6516\n  ], \n  [\n    1583712000.0, \n    7705\n  ], \n  [\n    1583715600.0, \n    6503\n  ], \n  [\n    1583719200.0, \n    7616\n  ], \n  [\n    1583722800.0, \n    6857\n  ], \n  [\n    1583726400.0, \n    9956\n  ]\n]", 
  "method": "GET", 
  "parameters": null, 
  "path_parameters": [
    {
      "description": "the slug of the organization for which the stats should be retrieved.", 
      "name": "organization_slug", 
      "type": "string"
    }
  ], 
  "query_parameters": [
    {
      "description": "the name of the stat to query (`\"received\"`, `\"rejected\"`, `\"blacklisted\"`)", 
      "name": "stat", 
      "type": "string"
    }, 
    {
      "description": "a timestamp to set the start of the query in seconds since UNIX epoch.", 
      "name": "since", 
      "type": "timestamp"
    }, 
    {
      "description": "a timestamp to set the end of the query in seconds since UNIX epoch.", 
      "name": "until", 
      "type": "timestamp"
    }, 
    {
      "description": "an explicit resolution to search for (one of `10s`, `1h`, and `1d`)", 
      "name": "resolution", 
      "type": "string"
    }
  ], 
  "sidebar_order": 20, 
  "title": "Retrieve Event Counts for an Organization", 
  "warning": "This endpoint may change in the future without notice."
}
---