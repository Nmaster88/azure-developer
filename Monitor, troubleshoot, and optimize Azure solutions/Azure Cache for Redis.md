You are developing an application that uses Azure Cache for Redis as a caching solution. The application must cache the response of an external service as a string value for 30 minutes.

You need to store the response in Azure Cache for Redis.

Which Azure Cache for Redis command should you use?

R:
You should use the SETEX command. You can use this command to store a value in a key and its expiration in a single operation. You should run
the command below to store a value in the key "myKey" for 30 minutes:

SETEX myKey 1800 "some-value"


--------------------------------------------------------
