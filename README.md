# postman-workflow-interpreter

# Data Type:

**data** Collection

**data** Environment

**data** Request

**data** Report

_getCollection :: [Request] -> Authorization -> PrerequestScript -> Tests -> Collection_

_interpret :: Collection -> Environment -> Environment -> (Environment, Report)_

```
Law: "interpret collection complete"
Forall: (c :: Collection), (r: Request), (e : Environment), (a: Authorization), (p: PrerequestScript), (t: Tests), (v: Variables), (re: Report).

interpret c e e = (e, re)
```

**data** Method

**data** Url

**data** Params

**data** Authorization

**data** Headers

**data** Body

**data** PrerequestScript

**data** Tests

**data** Settings

_getRequest :: Method -> Url -> Params -> Authorization -> Headers -> Body -> PrerequestScript -> Tests -> Settings -> Request_

_getRequestFields :: Request -> (Method, Url, Params, Authorization, Headers, Body, PrerequestScript, Tests, Settings)_
