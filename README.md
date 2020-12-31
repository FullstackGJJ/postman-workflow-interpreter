# postman-workflow-interpreter

# Data Type:

**data** Collection

**data** Environment

**data** Request

**data** Report

_getCollection :: [Request] -> Authorization -> PrerequestScript -> Tests -> Collection_

_interpret :: Collection -> Request -> Environment -> Environment -> (Environment, Report)_


```
Law: "interpret collection completion step"
Forall: (c :: Collection), (r: Request), (e : Environment), (a: Authorization), (p: PrerequestScript), (t: Tests), (v: Variables), (re: Report).

interpret c r e e = (e, re)
```

```
Law: "interpret collection starting/intermediate step"
Forall: (c :: Collection), (r: Request), (e : Environment), (a: Authorization), (p: PrerequestScript), (t: Tests), (v: Variables), (re: Report).

interpret c r e e = interpret c *r e e
```
<sub>* with r being the next request in sequence</sub>

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
