Enable diagnostics logging for apps in Azure App Service
check [link](https://learn.microsoft.com/en-us/azure/app-service/troubleshoot-diagnostic-logs)

# Enable application logging (Windows)

o enable application logging for Windows apps in the Azure portal, navigate to your app and select App Service logs.

Select On for either Application Logging (Filesystem) or Application Logging (Blob), or both.

The Filesystem option is for temporary debugging purposes, and turns itself off in 12 hours. The Blob option is for long-term logging, and needs a blob storage container to write logs to. The Blob option also includes additional information in the log messages, such as the ID of the origin VM instance of the log message (InstanceId), thread ID (Tid), and a more granular timestamp (EventTickCount).
