---
title: Lotus API

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true

code_clipboard: true

meta:
  - name: description
    content: "API documentation for Lotus - the reference Filecoin implementation."
---

# Introduction

This page contains all lotus API definitions. Interfaces defined here are exposed as JsonRPC 2.0 endpoints by lotus programs.

## $method_title

This is an example of how to structure a method for the docs.

$method_description

```shell
curl "api.chain.love" \
    -H "$method_shell_call_with_parameters"
```

```javascript
let outbound_request = new Request('$method_js_call_with_parameters');

fetch(outbound_request)
.then(function(response) {
    if (!response.ok) {
        throw new Error(`HTTP error! status: ${response.status}`);
    }
    return response.blob();
})
```

> The above command returns:

```json
$method_return_object
```

### Permissions

This endpoint require the following permissions: `$method_required_permissions` 

### Query parameters

This method requires the following parameters

| Name | Description | Default |
| ---- | ----------- | ------- |
| $parameter_name | $parameter_description | $parameter_default_value |

<!-- If there are no parameters, the following text is shown: -->
<!-- This method does not require any parameters. -->



# General

These methods are focused on general interactions between your client and a Lotus node. Most of these methods configure the node, and do not return any data.



## Closing

Close your connection to the Lotus node.

```shell
curl "api.chain.love" \
    -H "Closing: null"
```

```javascript
let outbound_request = new Request('closing');

fetch(outbound_request)
.then(function(response) {
    if (!response.ok) {
        throw new Error(`HTTP error! status: ${response.status}`);
    }
    return response.blob();
})
```

> The above command returns an empty object:

```json
[
    {
    }
]
```

### Permissions

This endpoint require the following permissions: `read`

### Query parameters

This method does not require any parameters.



## Discover

Returns key information about this Lotus node.

```shell
curl "api.chain.love" \
    -H "discover"
```

```javascript
let outbound_request = new Request('discover');

fetch(outbound_request)
.then(function(response) {
    if (!response.ok) {
        throw new Error(`HTTP error! status: ${response.status}`);
    }
    return response.blob();
})
```

> The above command returns:

```json
{
    "info": {
        "title": "Lotus RPC API",
            "version": "1.2.1/generated=2020-11-22T08:22:42-06:00"
    },
        "methods": [],
        "openrpc": "1.2.6"
}
```

### Permissions

This endpoint require the following permissions: `read` 

### Query parameters

This method does not require any parameters.



## Session

Returns the current session time.

```shell
curl "api.chain.love" \
    -H "session"
```

```javascript
let outbound_request = new Request('session');

fetch(outbound_request)
.then(function(response) {
    if (!response.ok) {
        throw new Error(`HTTP error! status: ${response.status}`);
    }
    return response.blob();
})
```

> The above command returns:

```json
[
    {
        "07070707-0707-0707-0707-070707070707"
    }
]
```

### Permissions

This endpoint require the following permissions: `read` 

### Query parameters

This method does not require any parameters.



## Shutdown

Shutsdown the Lotus node.

```shell
curl "api.chain.love" \
    -H "shutdown"
```

```javascript
let outbound_request = new Request('shutdown');

fetch(outbound_request)
.then(function(response) {
    if (!response.ok) {
        throw new Error(`HTTP error! status: ${response.status}`);
    }
    return response.blob();
})
```

> The above command returns an empty object:

```json
[
    {
    }
]
```

### Permissions

This endpoint require the following permissions: `admin` 

### Query parameters

This method does not require any parameters.



## Version

Returns the Lotus version number of this node.

```shell
curl "api.chain.love" \
    -H "version"
```

```javascript
let outbound_request = new Request('version');

fetch(outbound_request)
.then(function(response) {
    if (!response.ok) {
        throw new Error(`HTTP error! status: ${response.status}`);
    }
    return response.blob();
})
```

> The above command returns:

```json
{
  "Version": "string value",
  "APIVersion": 131328,
  "BlockDelay": 42
}
```

### Permissions

This endpoint require the following permissions: `read` 

### Query parameters

This method does not require any parameters.


## Auth

The following methods focus on authentication between your client and the Lotus node you are connecting to.

### AuthNew

Return an authorization token from a Lotus node.

```shell
curl "api.chain.love" \
    -H "authnew"
```

```javascript
let outbound_request = new Request('authnew');

fetch(outbound_request)
.then(function(response) {
    if (!response.ok) {
        throw new Error(`HTTP error! status: ${response.status}`);
    }
    return response.blob();
})
```

> If successful, the above command returns:

```json
[
    {
        "Ynl0ZSBhcnJheQ=="
    }
]
```

### Permissions

This endpoint require the following permissions: `admin` 

### Query parameters

This method does not require any parameters.

### AuthVerify

Verifies if an authorization token is valid.

```shell
curl "api.chain.love" \
    -H "authverify"
```

```javascript
let outbound_request = new Request('authverify');

fetch(outbound_request)
.then(function(response) {
    if (!response.ok) {
        throw new Error(`HTTP error! status: ${response.status}`);
    }
    return response.blob();
})
```

> If successful, the above command returns:

```json
[
    {
        "Ynl0ZSBhcnJheQ=="
    }
]
```
