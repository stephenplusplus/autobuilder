#Index

**Functions**

* [Topic(conn, name)](#Topic)
  * [topic.publish(data, callback)](#Topic#publish)
  * [topic.publishMessage(message, callback)](#Topic#publishMessage)
  * [topic.del(callback)](#Topic#del)
* [Connection()](#Connection)
  * [connection.listSubscriptions(callback)](#Connection#listSubscriptions)
  * [connection.getSubscription(name, callback)](#Connection#getSubscription)
  * [connection.subscribe(name)](#Connection#subscribe)
  * [connection.listTopics(callback)](#Connection#listTopics)
  * [connection.getTopic(name, callback)](#Connection#getTopic)
  * [connection.createTopic(name, callback)](#Connection#createTopic)
  * [connection.fullTopicName_()](#Connection#fullTopicName_)
  * [connection.fullProjectName_()](#Connection#fullProjectName_)

**Members**

* [PUBSUB_BASE_URL](#PUBSUB_BASE_URL)
* [SCOPES](#SCOPES)
* [Connection](#Connection)
  * [connection.listSubscriptions(callback)](#Connection#listSubscriptions)
  * [connection.getSubscription(name, callback)](#Connection#getSubscription)
  * [connection.subscribe(name)](#Connection#subscribe)
  * [connection.listTopics(callback)](#Connection#listTopics)
  * [connection.getTopic(name, callback)](#Connection#getTopic)
  * [connection.createTopic(name, callback)](#Connection#createTopic)
  * [connection.fullTopicName_()](#Connection#fullTopicName_)
  * [connection.fullProjectName_()](#Connection#fullProjectName_)
* [Topic](#Topic)
  * [topic.publish(data, callback)](#Topic#publish)
  * [topic.publishMessage(message, callback)](#Topic#publishMessage)
  * [topic.del(callback)](#Topic#del)
* [Subscription](#Subscription)
  * [subscription.ack(ids, callback)](#Subscription#ack)
  * [subscription.pull(callback)](#Subscription#pull)
  * [subscription.startPulling_()](#Subscription#startPulling_)
  * [subscription.del(callback)](#Subscription#del)
  * [subscription.close()](#Subscription#close)
  * [subscription.emitMessage_()](#Subscription#emitMessage_)
  * [subscription.emitError_()](#Subscription#emitError_)
 
<a name="Topic"></a>
#Topic(conn, name)
Represents a Google Cloud Pub/Sub API topic.

**Params**

- conn <code>[Connection](#Connection)</code> - Authorized connection.  
- name `string` - Full name of the topic.  

<a name="Connection"></a>
#Connection()
Represents connection to Google Cloud Pub/Sub API.

**Params**

  - projectId `string` - Google Developers Console Project ID.  
  - email `string` - Service account email.  
  - pemFilePath `string` - Path to the pem file that contains your
                                 private key.  

<a name="PUBSUB_BASE_URL"></a>
#PUBSUB_BASE_URL
Base URL for Pub/Sub API.

**Type**: `String`  
<a name="SCOPES"></a>
#SCOPES
Required scopes for Pub/Sub API.

**Type**: `Array`  
<a name="Connection"></a>
#Connection
Exports Connection.

<a name="Topic"></a>
#Topic
Exports Topic.

<a name="Subscription"></a>
#Subscription
Exports Subscription.

