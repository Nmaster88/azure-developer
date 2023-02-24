You create an Azure Event Hub. You want to create a console application to retrieve all events from a specific partition.

You need to write code to accomplish your goal.

What should you do?

R:
We should implement the IEventProcessor interface. This interface defines a method named ProcessEventAsync that passes a collection of EventData instances representing the messages in the Event Hub.

--------------

You want to use an Event Hub to store data from devices in a home alarm system. Each device runs .NET Core.

You need to ensure that the messages are delivered to the Event Hub in order across all devices.

What should you do?

R: Use the same partition key.
