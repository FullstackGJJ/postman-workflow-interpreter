# postman-workflow-interpreter

# Data Type:

**data** Collection

**data** Environment

**data** Request

**data** Result

_getCollection :: [Request] -> Authorization -> PrerequestScript -> Tests -> Collection_

_interpret :: Collection -> Environment -> Environment -> (Environment, Result)_

```
Law: "interpret collection"
Forall: (c :: Collection), (r: Request), (e : Environment), (a: Authorization), (p: PrerequestScript), (t: Tests), (v: Variables).

interpret c e e = interpret (getCollection [r] a p t v) e e
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
