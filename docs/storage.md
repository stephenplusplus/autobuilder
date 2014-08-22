<a name="module_storage"></a>
#storage
**Members**

* [storage](#module_storage)
  * [storage~conn](#module_storage..conn)
  * [storage~util](#module_storage..util)
  * [storage~Bucket(options)](#module_storage..Bucket)
    * [bucket.list([query], callback)](#module_storage..Bucket#list)
    * [bucket.stat(name, callback)](#module_storage..Bucket#stat)
    * [bucket.copy(name, metadata, [callback])](#module_storage..Bucket#copy)
    * [bucket.remove(name, callback)](#module_storage..Bucket#remove)
    * [bucket.createReadStream(name)](#module_storage..Bucket#createReadStream)
    * [bucket.createWriteStream(name, [metadata])](#module_storage..Bucket#createWriteStream)
    * [bucket.write(name, options, [callback])](#module_storage..Bucket#write)
    * [bucket.getWritableStream_(name, metadata, callback)](#module_storage..Bucket#getWritableStream_)
    * [bucket.makeReq(method, path, query, body, callback)](#module_storage..Bucket#makeReq)
  * [const: storage~SCOPES](#module_storage..SCOPES)
  * [const: storage~STORAGE_BASE_URL](#module_storage..STORAGE_BASE_URL)
  * [const: storage~STORAGE_UPLOAD_BASE_URL](#module_storage..STORAGE_UPLOAD_BASE_URL)

<a name="module_storage..conn"></a>
##storage~conn
**Scope**: inner member of [storage](#module_storage)  
**Type**: [module:common/connection](module:common/connection)  
<a name="module_storage..util"></a>
##storage~util
**Scope**: inner member of [storage](#module_storage)  
**Type**: [module:common/util](module:common/util)  
<a name="module_storage..Bucket"></a>
##storage~Bucket(options)
Google Cloud Storage allows you to store data on Google infrastructure. See
the guide on [https://developers.google.com/storage](https://developers.google.com/storage) to create a
bucket.

**Params**

- options `object` - Configuration options.  
  - bucketName `string` - Name of the bucket.  
  - keyFileName `string` - Full path to the JSON key downloaded
    from the Google Developers Console.  

**Scope**: inner function of [storage](#module_storage)  
**Example**  
```js
var gcloud = require('gcloud');
var bucket;

// From Google Compute Engine
bucket = new gcloud.storage.Bucket({
  bucketName: YOUR_BUCKET_NAME
});

// From elsewhere
bucket = new gcloud.storage.Bucket({
  bucketName: YOUR_BUCKET_NAME,
  keyFilename: '/path/to/the/key.json'
});
```

<a name="module_storage..SCOPES"></a>
##const: storage~SCOPES
Required scopes for Google Cloud Storage API.

**Scope**: inner constant of [storage](#module_storage)  
**Type**: `array`  
<a name="module_storage..STORAGE_BASE_URL"></a>
##const: storage~STORAGE_BASE_URL
**Scope**: inner constant of [storage](#module_storage)  
**Type**: `string`  
<a name="module_storage..STORAGE_UPLOAD_BASE_URL"></a>
##const: storage~STORAGE_UPLOAD_BASE_URL
**Scope**: inner constant of [storage](#module_storage)  
**Type**: `string`  
