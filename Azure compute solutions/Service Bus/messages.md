https://learn.microsoft.com/en-us/dotnet/api/azure.messaging.servicebus.servicebusmessage?view=azure-dotnet

The ServiceBusMessage is used to send data to Service Bus Queues and Topics. When receiving messages, the ServiceBusReceivedMessage is used.

The properties are the following:

|property|description|
|-|-|
|ApplicationProperties|Gets the application properties bag, which can be used for custom message metadata.|
|Body|Gets or sets the body of the message.|
|ContentType|Gets or sets the content type descriptor.|
|CorrelationId|Gets or sets the a correlation identifier.|
|MessageId|Gets or sets the MessageId to identify the message.|
|PartitionKey|Gets or sets a partition key for sending a message to a partitioned entity.|
|ReplyTo|Gets or sets the address of an entity to send replies to.|
|ReplyToSessionId|Gets or sets a session identifier augmenting the ReplyTo address.|
|ScheduledEnqueueTime|Gets or sets the date and time in UTC at which the message will be enqueued. This property returns the time in UTC; when setting the property, the supplied DateTime value must also be in UTC.|
|SessionId|Gets or sets the session identifier for a session-aware entity.|
|Subject|Gets or sets an application specific subject.|
|TimeToLive|Gets or sets the message’s "time to live" value.|
|To|Gets or sets the "to" address.|
|TransactionPartitionKey|Gets or sets a partition key for sending a message into an entity via a partitioned transfer queue.|
