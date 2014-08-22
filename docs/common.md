#Index

**Modules**

* [common/connection](#module_common/connection)
  * [common/connection~util](#module_common/connection..util)
  * [common/connection~Connection(opts)](#module_common/connection..Connection)
    * [connection.requester](#module_common/connection..Connection#requester)
    * [connection.connect(callback)](#module_common/connection..Connection#connect)
    * [connection.fetchToken(callback)](#module_common/connection..Connection#fetchToken)
    * [connection.req(requestOptions, [callback])](#module_common/connection..Connection#req)
    * [connection.createAuthorizedReq(requestOptions, callback)](#module_common/connection..Connection#createAuthorizedReq)
    * [connection.isConnected()](#module_common/connection..Connection#isConnected)
    * [connection.authorizeReq(requestOptions)](#module_common/connection..Connection#authorizeReq)
  * [const: common/connection~Base](#module_common/connection..Base)
  * [const: common/connection~gcloud-node's](#module_common/connection..gcloud-node's)
  * [const: common/connection~User](#module_common/connection..User)
  * [class: common/connection~Token](#module_common/connection..Token)
    * [new common/connection~Token(accessToken, expiry)](#new_module_common/connection..Token)
    * [token.isExpired()](#module_common/connection..Token#isExpired)
* [common/util](#module_common/util)
  * [common/util~extend(from, to)](#module_common/util..extend)
  * [common/util~arrayize(input)](#module_common/util..arrayize)
  * [common/util~format(template, args)](#module_common/util..format)
  * [common/util~noop()](#module_common/util..noop)
  * [common/util~handleResp(err, resp, body, callback)](#module_common/util..handleResp)
 
<a name="module_common/connection"></a>
#common/connection
**Members**

* [common/connection](#module_common/connection)
  * [common/connection~util](#module_common/connection..util)
  * [common/connection~Connection(opts)](#module_common/connection..Connection)
    * [connection.requester](#module_common/connection..Connection#requester)
    * [connection.connect(callback)](#module_common/connection..Connection#connect)
    * [connection.fetchToken(callback)](#module_common/connection..Connection#fetchToken)
    * [connection.req(requestOptions, [callback])](#module_common/connection..Connection#req)
    * [connection.createAuthorizedReq(requestOptions, callback)](#module_common/connection..Connection#createAuthorizedReq)
    * [connection.isConnected()](#module_common/connection..Connection#isConnected)
    * [connection.authorizeReq(requestOptions)](#module_common/connection..Connection#authorizeReq)
  * [const: common/connection~Base](#module_common/connection..Base)
  * [const: common/connection~gcloud-node's](#module_common/connection..gcloud-node's)
  * [const: common/connection~User](#module_common/connection..User)
  * [class: common/connection~Token](#module_common/connection..Token)
    * [new common/connection~Token(accessToken, expiry)](#new_module_common/connection..Token)
    * [token.isExpired()](#module_common/connection..Token#isExpired)

<a name="module_common/connection..util"></a>
##common/connection~util
**Scope**: inner member of [common/connection](#module_common/connection)  
**Type**: [common/util](#module_common/util)  
<a name="module_common/connection..Connection"></a>
##common/connection~Connection(opts)
Create a connection object.

**Params**

- opts `object` - Configuration options.  
  - scopes `array` - Scopes required for access.  

**Scope**: inner function of [common/connection](#module_common/connection)  
**Example**  
```js
var SCOPES = [
  'https://www.googleapis.com/auth/datastore',
  'https://www.googleapis.com/auth/userinfo.email'
];
var conn = new Connection({ scopes: SCOPES });
```

<a name="module_common/connection..Base"></a>
##const: common/connection~Base
URL for outgoing requests.

**Scope**: inner constant of [common/connection](#module_common/connection)  
**Type**: `string`  
<a name="module_common/connection..gcloud-node's"></a>
##const: common/connection~gcloud-node's
package.json file.

**Scope**: inner constant of [common/connection](#module_common/connection)  
**Type**: `object`  
<a name="module_common/connection..User"></a>
##const: common/connection~User
agent.

**Scope**: inner constant of [common/connection](#module_common/connection)  
**Type**: `string`  
<a name="module_common/connection..Token"></a>
##class: common/connection~Token
**Members**

* [class: common/connection~Token](#module_common/connection..Token)
  * [new common/connection~Token(accessToken, expiry)](#new_module_common/connection..Token)
  * [token.isExpired()](#module_common/connection..Token#isExpired)

<a name="new_module_common/connection..Token"></a>
###new common/connection~Token(accessToken, expiry)
Token represents an access token.

**Params**

- accessToken `string` - Access token.  
- expiry `date` - Expiration datetime.  

**Scope**: inner class of [common/connection](#module_common/connection)  
**Example**  
```js
var token = new Token(ACCESS_TOKEN, EXPIRY);
```

<a name="module_common/connection..Token#isExpired"></a>
###token.isExpired()
Is this token expired?

**Returns**: `boolean`  
**Example**  
```js
token.isExpired();
```

<a name="module_common/util"></a>
#common/util
**Members**

* [common/util](#module_common/util)
  * [common/util~extend(from, to)](#module_common/util..extend)
  * [common/util~arrayize(input)](#module_common/util..arrayize)
  * [common/util~format(template, args)](#module_common/util..format)
  * [common/util~noop()](#module_common/util..noop)
  * [common/util~handleResp(err, resp, body, callback)](#module_common/util..handleResp)

<a name="module_common/util..extend"></a>
##common/util~extend(from, to)
Extend a base object with properties from another.

**Params**

- from `object` - The base object.  
- to `object` - The object to extend with.  

**Scope**: inner function of [common/util](#module_common/util)  
**Returns**: `object` - ```  
<a name="module_common/util..arrayize"></a>
##common/util~arrayize(input)
Wrap an array around a non-Array object. If given an Array, it is returned.

**Params**

- input `*` - Non-array object to wrap.  

**Scope**: inner function of [common/util](#module_common/util)  
**Returns**: `array`  
**Example**  
```js
arrayize(2);
// [ 2 ]

arrayize(['Hi']);
// [ 'Hi' ]
```

<a name="module_common/util..format"></a>
##common/util~format(template, args)
Format a string with values from the provided object.

**Params**

- template `string` - String with {} denoted keys. (See example)  
- args `object` - Key/value pairs matching the holes in the template.  

**Scope**: inner function of [common/util](#module_common/util)  
**Returns**: `string`  
**Example**  
```js
format('This is a {language} ({abbr}) codebase.', {
  language: 'JavaScript',
  abbr: 'JS'
});
// 'This is a JavaScript (JS) codebase.'
```

<a name="module_common/util..noop"></a>
##common/util~noop()
No op.

**Scope**: inner function of [common/util](#module_common/util)  
**Example**  
```js
function doSomething(callback) {
  callback = callback || noop;
}
```

<a name="module_common/util..handleResp"></a>
##common/util~handleResp(err, resp, body, callback)
Uniformly process an API response.

**Params**

- err `*` - Error value.  
- resp `*` - Response value.  
- body `*` - Body value.  
- callback `function` - The callback function.  

**Scope**: inner function of [common/util](#module_common/util)  
