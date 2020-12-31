# postman-workflow-interpreter

# Data Type:

**data** Collection

**data** Environment

**data** Request

**data** Result

getCollection :: [Request] -> Authorization -> PrerequestScript -> Tests -> Collection

interpret :: Collection -> Environment -> Environment -> (Environment, Result)

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

getRequest :: Method -> Url -> Params -> Authorization -> Headers -> Body -> PrerequestScript -> Tests -> Settings -> Request

getRequestFields :: Request -> (Method, Url, Params, Authorization, Headers, Body, PrerequestScript, Tests, Settings)
