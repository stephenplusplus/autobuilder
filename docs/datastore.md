#Index

**Modules**

* [datastore/dataset](#module_datastore/dataset)
  * [class: Dataset ⏏](#exp_module_datastore/dataset)
    * [new Dataset(options)](#exp_new_module_datastore/dataset)
    * [datastore/dataset~conn](#module_datastore/dataset..conn)
    * [datastore/dataset~entity](#module_datastore/dataset..entity)
    * [datastore/dataset~pb](#module_datastore/dataset..pb)
    * [datastore/dataset~Query](#module_datastore/dataset..Query)
    * [datastore/dataset~Transaction](#module_datastore/dataset..Transaction)
    * [datastore/dataset~util](#module_datastore/dataset..util)
    * [datastore/dataset.createQuery()](#module_datastore/dataset#createQuery)
    * [datastore/dataset.get()](#module_datastore/dataset#get)
    * [datastore/dataset.save()](#module_datastore/dataset#save)
    * [datastore/dataset.delete()](#module_datastore/dataset#delete)
    * [datastore/dataset.runQuery()](#module_datastore/dataset#runQuery)
    * [datastore/dataset.runInTransaction(fn, callback)](#module_datastore/dataset#runInTransaction)
    * [datastore/dataset.allocateIds(incompleteKey, n, callback)](#module_datastore/dataset#allocateIds)
    * [const: datastore/dataset~SCOPES](#module_datastore/dataset..SCOPES)
* [datastore/entity](#module_datastore/entity)
  * [class: datastore/entity~Key](#module_datastore/entity..Key)
    * [new datastore/entity~Key()](#new_module_datastore/entity..Key)
  * [class: datastore/entity~Int](#module_datastore/entity..Int)
    * [new datastore/entity~Int(val)](#new_module_datastore/entity..Int)
    * [int.get()](#module_datastore/entity..Int#get)
  * [class: datastore/entity~Double](#module_datastore/entity..Double)
    * [new datastore/entity~Double(val)](#new_module_datastore/entity..Double)
    * [double.get()](#module_datastore/entity..Double#get)
* [datastore](#module_datastore)
  * [datastore ⏏](#exp_module_datastore)
    * [datastore~entity](#module_datastore..entity)
    * [datastore.Dataset](#module_datastore.Dataset)
    * [datastore.key()](#module_datastore.key)
    * [datastore.int()](#module_datastore.int)
    * [datastore.double()](#module_datastore.double)
* [datastore/pb](#module_datastore/pb)
  * [module.exports ⏏](#exp_module_datastore/pb)
    * [const: datastore/pb~Path](#module_datastore/pb..Path)
* [datastore/transaction](#module_datastore/transaction)
  * [class: Transaction ⏏](#exp_module_datastore/transaction)
    * [new Transaction(conn, datasetId)](#exp_new_module_datastore/transaction)
    * [datastore/transaction~entity](#module_datastore/transaction..entity)
    * [datastore/transaction~pb](#module_datastore/transaction..pb)
    * [datastore/transaction~util](#module_datastore/transaction..util)
    * [datastore/transaction.begin(callback)](#module_datastore/transaction#begin)
    * [datastore/transaction.rollback(callback)](#module_datastore/transaction#rollback)
    * [datastore/transaction.commit(callback)](#module_datastore/transaction#commit)
    * [datastore/transaction.finalize(callback)](#module_datastore/transaction#finalize)
    * [datastore/transaction.get(key, callback)](#module_datastore/transaction#get)
    * [datastore/transaction.save(entities, callback)](#module_datastore/transaction#save)
    * [datastore/transaction.delete(key, callback)](#module_datastore/transaction#delete)
    * [datastore/transaction.runQuery(query, callback)](#module_datastore/transaction#runQuery)
    * [datastore/transaction.mapQuery()](#module_datastore/transaction#mapQuery)
    * [datastore/transaction.makeReq(method, req, callbcak)](#module_datastore/transaction#makeReq)
    * [const: datastore/transaction~Host](#module_datastore/transaction..Host)
    * [const: datastore/transaction~Non-transaction](#module_datastore/transaction..Non-transaction)
    * [const: datastore/transaction~Transaction](#module_datastore/transaction..Transaction)
 
<a name="module_datastore/dataset"></a>
#datastore/dataset
<a name="exp_module_datastore/dataset"></a>
##class: Dataset ⏏
**Members**

* [class: Dataset ⏏](#exp_module_datastore/dataset)
  * [new Dataset(options)](#exp_new_module_datastore/dataset)
  * [datastore/dataset~conn](#module_datastore/dataset..conn)
  * [datastore/dataset~entity](#module_datastore/dataset..entity)
  * [datastore/dataset~pb](#module_datastore/dataset..pb)
  * [datastore/dataset~Query](#module_datastore/dataset..Query)
  * [datastore/dataset~Transaction](#module_datastore/dataset..Transaction)
  * [datastore/dataset~util](#module_datastore/dataset..util)
  * [datastore/dataset.createQuery()](#module_datastore/dataset#createQuery)
  * [datastore/dataset.get()](#module_datastore/dataset#get)
  * [datastore/dataset.save()](#module_datastore/dataset#save)
  * [datastore/dataset.delete()](#module_datastore/dataset#delete)
  * [datastore/dataset.runQuery()](#module_datastore/dataset#runQuery)
  * [datastore/dataset.runInTransaction(fn, callback)](#module_datastore/dataset#runInTransaction)
  * [datastore/dataset.allocateIds(incompleteKey, n, callback)](#module_datastore/dataset#allocateIds)
  * [const: datastore/dataset~SCOPES](#module_datastore/dataset..SCOPES)

<a name="exp_new_module_datastore/dataset"></a>
###new Dataset(options)
Intract with a dataset from the
[Google Cloud Datastore](https://developers.google.com/datastore/).

**Params**

- options `object`  
  - id `string` - Dataset ID. This is your project ID from the
    Google Developers Console.  
  - keyFileName `string` - Full path to the JSON key downloaded
    from the Google Developers Console.  

**Example**  
```js
var dataset = new Dataset({
  id: 'my-project',
  keyFileName: '/path/to/keyfile.json'
});
```

<a name="module_datastore/dataset..conn"></a>
###datastore/dataset~conn
**Scope**: inner member of [datastore/dataset](#module_datastore/dataset)  
**Type**: [module:common/connection](module:common/connection)  
<a name="module_datastore/dataset..entity"></a>
###datastore/dataset~entity
**Scope**: inner member of [datastore/dataset](#module_datastore/dataset)  
**Type**: [datastore/entity](#module_datastore/entity)  
<a name="module_datastore/dataset..pb"></a>
###datastore/dataset~pb
**Scope**: inner member of [datastore/dataset](#module_datastore/dataset)  
**Type**: [datastore/pb](#module_datastore/pb)  
<a name="module_datastore/dataset..Query"></a>
###datastore/dataset~Query
**Scope**: inner member of [datastore/dataset](#module_datastore/dataset)  
**Type**: [module:datastore/query](#module_datastore/query)  
<a name="module_datastore/dataset..Transaction"></a>
###datastore/dataset~Transaction
**Scope**: inner member of [datastore/dataset](#module_datastore/dataset)  
**Type**: [datastore/transaction](#module_datastore/transaction)  
<a name="module_datastore/dataset..util"></a>
###datastore/dataset~util
**Scope**: inner member of [datastore/dataset](#module_datastore/dataset)  
**Type**: [module:common/util](module:common/util)  
<a name="module_datastore/dataset#createQuery"></a>
###datastore/dataset.createQuery()
Create a query from the current dataset to query the specified kinds.

**Returns**: [module:datastore/query](#module_datastore/query)  
**Example**  
```js
var query = dataset.createQuery(['Lion', 'Chimp']);
var zooQuery = dataset.createQuery('zoo', ['Lion', 'Chimp']);
```

<a name="module_datastore/dataset#get"></a>
###datastore/dataset.get()
**Example**  
```js
dataset.get([
  datastore.key('Company', 123),
  datastore.key('Product', 'Computer')
], function(err, entities) {});
```

<a name="module_datastore/dataset#save"></a>
###datastore/dataset.save()
**Example**  
```js
// Save a single entity.
dataset.save({
  key: datastore.key('Company', null),
  data: {
    rating: '10'
  }
}, function(err, key) {
  // Because we gave an incomplete key as an argument, `key` will be
  // populated with the complete, generated key.
});

// Save multiple entities at once.
dataset.save([
  {
    key: datastore.key('Company', 123),
    data: {
      HQ: 'Dallas, TX'
    }
  },
  {
    key: datastore.key('Product', 'Computer'),
    data: {
      vendor: 'Dell'
    }
  }
], function(err, keys) {});
```

<a name="module_datastore/dataset#delete"></a>
###datastore/dataset.delete()
**Example**  
```js
// Delete a single entity.
dataset.delete(datastore.key('Company', 123), function(err) {});

// Delete multiple entities at once.
dataset.delete([
  datastore.key('Company', 123),
  datastore.key('Product', 'Computer')
], function(err) {});
```

<a name="module_datastore/dataset#runQuery"></a>
###datastore/dataset.runQuery()
**Example**  
```js
// Retrieve 5 companies.
dataset.runQuery(queryObject, function(err, entities, nextQuery) {
  // `nextQuery` is not null if there are more results.
  if (nextQuery) {
    dataset.runQuery(nextQuery, function(err, entities, nextQuery) {});
  }
});
```

<a name="module_datastore/dataset#runInTransaction"></a>
###datastore/dataset.runInTransaction(fn, callback)
Run a function in the context of a new transaction. Transactions allow you to
perform multiple operations, committing your changes atomically.

**Params**

- fn `function` - The function to run in the context of a transaction.  
- callback `function` - The callback function.  

**Example**  
```js
dataset.transaction(function(transaction, done) {
  // From the `transaction` object, execute dataset methods as usual.
  // Call `done` when you're ready to commit all of the changes.
  transaction.get(datastore.key('Company', 123), function(err, entity) {
    if (err) {
      transaction.rollback(done);
      return;
    }

    done();
  });
}, function(err) {});
```

<a name="module_datastore/dataset#allocateIds"></a>
###datastore/dataset.allocateIds(incompleteKey, n, callback)
Generate IDs without creating entities.

**Params**

- incompleteKey `Key` - The key object to complete.  
- n `number` - How many IDs to generate.  
- callback `function` - The callback function.  

**Example**  
```js
// The following call will create 100 new IDs from the Company kind, which
// exists under the default namespace.
var incompleteKey = datastore.key('Company', null);
dataset.allocateIds(incompleteKey, 100, function(err, keys) {});

// You may prefer to create IDs from a non-default namespace by providing an
// incomplete key with a namespace. Similar to the previous example, the call
// below will create 100 new IDs, but from the Company kind that exists under
// the "ns-test" namespace.
var incompleteKey = datastore.key('ns-test', 'Company', null);
dataset.allocateIds(incompleteKey, 100, function(err, keys) {});
```

<a name="module_datastore/dataset..SCOPES"></a>
###const: datastore/dataset~SCOPES
Scopes for Google Datastore access.

**Scope**: inner constant of [datastore/dataset](#module_datastore/dataset)  
**Type**: `array`  
<a name="module_datastore/entity"></a>
#datastore/entity
**Members**

* [datastore/entity](#module_datastore/entity)
  * [class: datastore/entity~Key](#module_datastore/entity..Key)
    * [new datastore/entity~Key()](#new_module_datastore/entity..Key)
  * [class: datastore/entity~Int](#module_datastore/entity..Int)
    * [new datastore/entity~Int(val)](#new_module_datastore/entity..Int)
    * [int.get()](#module_datastore/entity..Int#get)
  * [class: datastore/entity~Double](#module_datastore/entity..Double)
    * [new datastore/entity~Double(val)](#new_module_datastore/entity..Double)
    * [double.get()](#module_datastore/entity..Double#get)

<a name="module_datastore/entity..Key"></a>
##class: datastore/entity~Key
**Members**

* [class: datastore/entity~Key](#module_datastore/entity..Key)
  * [new datastore/entity~Key()](#new_module_datastore/entity..Key)

<a name="new_module_datastore/entity..Key"></a>
###new datastore/entity~Key()
Build a Datastore Key object.

**Params**

- ... `*` - Key descriptors.  

**Scope**: inner class of [datastore/entity](#module_datastore/entity)  
**Example**  
```js
var key = new Key('Company', 123);
```

<a name="module_datastore/entity..Int"></a>
##class: datastore/entity~Int
**Members**

* [class: datastore/entity~Int](#module_datastore/entity..Int)
  * [new datastore/entity~Int(val)](#new_module_datastore/entity..Int)
  * [int.get()](#module_datastore/entity..Int#get)

<a name="new_module_datastore/entity..Int"></a>
###new datastore/entity~Int(val)
Build a Datastore Int object.

**Params**

- val `number` - The integer value.  

**Scope**: inner class of [datastore/entity](#module_datastore/entity)  
**Example**  
```js
var anInt = new Int(7);
```

<a name="module_datastore/entity..Int#get"></a>
###int.get()
Retrieve the Integer value.

**Returns**: `number`  
<a name="module_datastore/entity..Double"></a>
##class: datastore/entity~Double
**Members**

* [class: datastore/entity~Double](#module_datastore/entity..Double)
  * [new datastore/entity~Double(val)](#new_module_datastore/entity..Double)
  * [double.get()](#module_datastore/entity..Double#get)

<a name="new_module_datastore/entity..Double"></a>
###new datastore/entity~Double(val)
Build a Datastore Double object.

**Params**

- val `number` - The double value.  

**Scope**: inner class of [datastore/entity](#module_datastore/entity)  
**Example**  
```js
var aDouble = new Double(7);
```

<a name="module_datastore/entity..Double#get"></a>
###double.get()
Retrieve the Integer value.

**Returns**: `number`  
<a name="module_datastore"></a>
#datastore
**Members**

* [datastore](#module_datastore)
  * [datastore ⏏](#exp_module_datastore)
    * [datastore~entity](#module_datastore..entity)
    * [datastore.Dataset](#module_datastore.Dataset)
    * [datastore.key()](#module_datastore.key)
    * [datastore.int()](#module_datastore.int)
    * [datastore.double()](#module_datastore.double)

<a name="module_datastore..entity"></a>
##datastore~entity
**Scope**: inner member of [datastore](#module_datastore)  
**Type**: [datastore/entity](#module_datastore/entity)  
<a name="module_datastore.Dataset"></a>
##datastore.Dataset
**Example**  
```js
var dataset = new datastore.Dataset();
```

<a name="module_datastore.key"></a>
##datastore.key()
**Example**  
```js
var key = dataset.key('Company', 123);
```

<a name="module_datastore.int"></a>
##datastore.int()
**Example**  
```js
var anInteger = dataset.int(7);
```

<a name="module_datastore.double"></a>
##datastore.double()
Helper function to get a Datastore Double object.

**Example**  
```js
var aDouble = dataset.double(7);
```

<a name="module_datastore/pb"></a>
#datastore/pb
<a name="module_datastore/pb..Path"></a>
##const: datastore/pb~Path
to the proto file.

**Scope**: inner constant of [datastore/pb](#module_datastore/pb)  
**Type**: `string`  
<a name="module_datastore/transaction"></a>
#datastore/transaction
<a name="exp_module_datastore/transaction"></a>
##class: Transaction ⏏
**Members**

* [class: Transaction ⏏](#exp_module_datastore/transaction)
  * [new Transaction(conn, datasetId)](#exp_new_module_datastore/transaction)
  * [datastore/transaction~entity](#module_datastore/transaction..entity)
  * [datastore/transaction~pb](#module_datastore/transaction..pb)
  * [datastore/transaction~util](#module_datastore/transaction..util)
  * [datastore/transaction.begin(callback)](#module_datastore/transaction#begin)
  * [datastore/transaction.rollback(callback)](#module_datastore/transaction#rollback)
  * [datastore/transaction.commit(callback)](#module_datastore/transaction#commit)
  * [datastore/transaction.finalize(callback)](#module_datastore/transaction#finalize)
  * [datastore/transaction.get(key, callback)](#module_datastore/transaction#get)
  * [datastore/transaction.save(entities, callback)](#module_datastore/transaction#save)
  * [datastore/transaction.delete(key, callback)](#module_datastore/transaction#delete)
  * [datastore/transaction.runQuery(query, callback)](#module_datastore/transaction#runQuery)
  * [datastore/transaction.mapQuery()](#module_datastore/transaction#mapQuery)
  * [datastore/transaction.makeReq(method, req, callbcak)](#module_datastore/transaction#makeReq)
  * [const: datastore/transaction~Host](#module_datastore/transaction..Host)
  * [const: datastore/transaction~Non-transaction](#module_datastore/transaction..Non-transaction)
  * [const: datastore/transaction~Transaction](#module_datastore/transaction..Transaction)

<a name="exp_new_module_datastore/transaction"></a>
###new Transaction(conn, datasetId)
Build a Transaction object. Transactions will generally be built for you by
{@linkcode module:datastore/dataset}. When you need to run a transactional
operation, you use {@linkcode module:datastore/dataset#runInTransaction}.

*Reference: [http://goo.gl/n4oSjt](http://goo.gl/n4oSjt)*

**Params**

- conn <code>[module:common/connection.Connection](module:common/connection.Connection)</code> - An authorized connection
    to Google Cloud Datastore.  
- datasetId `string` - Dataset ID. This is your project ID from the
    Google Developers Console.  

**Example**  
```js
var Connection = require('lib/common/connection.js').Connection;
var myConnection = new Connection({});
var transaction = new Transaction(myConnection, 'my-project-id');
```

<a name="module_datastore/transaction..entity"></a>
###datastore/transaction~entity
**Scope**: inner member of [datastore/transaction](#module_datastore/transaction)  
**Type**: [datastore/entity](#module_datastore/entity)  
<a name="module_datastore/transaction..pb"></a>
###datastore/transaction~pb
**Scope**: inner member of [datastore/transaction](#module_datastore/transaction)  
**Type**: [datastore/pb](#module_datastore/pb)  
<a name="module_datastore/transaction..util"></a>
###datastore/transaction~util
**Scope**: inner member of [datastore/transaction](#module_datastore/transaction)  
**Type**: [module:common/util](module:common/util)  
<a name="module_datastore/transaction#begin"></a>
###datastore/transaction.begin(callback)
Begin a remote transaction and identify the current transaction instance with
the remote transaction's ID.

**Params**

- callback `function` - The function to execute within the context of
    a transaction.  

**Example**  
```js
transaction.begin(function(err) {
  // Perform Datastore operations as usual.
  transaction.get(datastore.key('Company', 123), function(err, entity) {
    // Commit the transaction.
    transaction.finalize(function(err) {});

    // Rollback the transaction.
    transaction.rollback(function(err) {});
  });
});
```

<a name="module_datastore/transaction#rollback"></a>
###datastore/transaction.rollback(callback)
Reverse a transaction remotely and finalize the current transaction instance.

**Params**

- callback `function` - The callback function.  

**Example**  
```js
transaction.begin(function(err) {
  transaction.rollback(function(err) {
    if (err) {
      // Transaction could not be rolled back.
    }
  });
});
```

<a name="module_datastore/transaction#commit"></a>
###datastore/transaction.commit(callback)
Commit the remote transaction and finalize the current transaction instance.

**Params**

- callback `function` - The callback function.  

**Example**  
```js
transaction.begin(function(err) {
  transaction.commit(function(err) {
    if (err) {
      // Transaction could not be committed.
    }
  });
});
```

<a name="module_datastore/transaction#finalize"></a>
###datastore/transaction.finalize(callback)
Commit a transaction if it's not finalized yet.

**Params**

- callback `function` - The callback function.  

**Example**  
```js
transaction.begin(function(err) {
  transaction.finalize(function(err) {
    if (err) {
      // Transaction could not be finalized.
    }
  });
});
```

<a name="module_datastore/transaction#get"></a>
###datastore/transaction.get(key, callback)
Retrieve the entities identified with the specified key(s) in the current
transaction. Get operations require a valid key to retrieve the
key-identified entity from Datastore.

**Params**

- key <code>[Key](#module_datastore/entity..Key)</code> | <code>[Array.&lt;Key&gt;](#module_datastore/entity..Key)</code> - Datastore key object(s).  
- callback `function` - The callback function.  

**Example**  
```js
// These examples work with both a Transaction object and a Dataset object.

// Get a single entity.
transaction.get(datastore.key('Company', 123), function(err, entity));

// Get multiple entities at once.
transaction.get([
  datastore.key('Company', 123),
  datastore.key('Product', 'Computer')
], function(err, entities) {});
```

<a name="module_datastore/transaction#save"></a>
###datastore/transaction.save(entities, callback)
Insert or update the specified object(s) in the current transaction. If a
key is incomplete, its associated object is inserted and its generated
identifier is returned to the callback.

**Params**

- entities `object` | `Array.<object>` - Datastore key object(s).  
  - key `Key` - Datastore key object.  
  - data `object` - Data to save with the provided key.  
- callback `function` - The callback function.  

**Example**  
```js
// These examples work with both a Transaction object and a Dataset object.

// Save a single entity.
transaction.save({
  key: datastore.key('Company', null),
  data: {
    rating: '10'
  }
}, function(err, key) {
  // Because we gave an incomplete key as an argument, `key` will be
  // populated with the complete, generated key.
});

// Save multiple entities at once.
transaction.save([
  {
    key: datastore.key('Company', 123),
    data: {
      HQ: 'Dallas, TX'
    }
  },
  {
    key: datastore.key('Product', 'Computer'),
    data: {
      vendor: 'Dell'
    }
  }
], function(err, keys) {});
```

<a name="module_datastore/transaction#delete"></a>
###datastore/transaction.delete(key, callback)
Delete all entities identified with the specified key(s) in the current
transaction.

**Params**

- key `Key` | `Array.<Key>` - Datastore key object(s).  
- callback `function` - The callback function.  

**Example**  
```js
// These examples work with both a Transaction object and a Dataset object.

// Delete a single entity.
transaction.delete(datastore.key('Company', 123), function(err) {});

// Delete multiple entities at once.
transaction.delete([
  datastore.key('Company', 123),
  datastore.key('Product', 'Computer')
], function(err) {});
```

<a name="module_datastore/transaction#runQuery"></a>
###datastore/transaction.runQuery(query, callback)
Datastore allows you to query entities by kind, filter them by property
filters, and sort them by a property name. Projection and pagination are also
supported. If more results are available, a query to retrieve the next page
is provided to the callback function.

**Params**

- query `Query` - Query object.  
- callback `function` - The callback function.  

**Example**  
```js
// Retrieve 5 companies.
transaction.runQuery(queryObject, function(err, entities, nextQuery) {
  // `nextQuery` is not null if there are more results.
  if (nextQuery) {
    transaction.runQuery(nextQuery, function(err, entities, nextQuery) {});
  }
});
```

<a name="module_datastore/transaction#mapQuery"></a>
###datastore/transaction.mapQuery()
mapQuery

<a name="module_datastore/transaction#makeReq"></a>
###datastore/transaction.makeReq(method, req, callbcak)
Make a request to the API endpoint.

**Params**

- method `string` - Transaction action (allocateIds, commit, etc.).  
- req `object` - Request configuration object.  
- callbcak `function` - The callback function.  

**Example**  
```js
var deleteRequest = {
  MODE: 'NON_TRANSACTIONAL',
  mutation: {
    delete: [] // datastore key objects.
  }
};
transaction.makeReq('commit', deleteRequest, function(err) {});
```

<a name="module_datastore/transaction..Host"></a>
###const: datastore/transaction~Host
to send with API requests.

**Scope**: inner constant of [datastore/transaction](#module_datastore/transaction)  
**Type**: `string`  
<a name="module_datastore/transaction..Non-transaction"></a>
###const: datastore/transaction~Non-transaction
mode key.

**Scope**: inner constant of [datastore/transaction](#module_datastore/transaction)  
**Type**: `string`  
<a name="module_datastore/transaction..Transaction"></a>
###const: datastore/transaction~Transaction
mode key.

**Scope**: inner constant of [datastore/transaction](#module_datastore/transaction)  
**Type**: `string`  
