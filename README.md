AzureCommandLineTools
=====================

Simple command line tools for interacting with Windows Azure Storage. A work in progress.

Before running these commands you need to set an environment variable with your azure storage configuration details. Most people will need something like this:

SET AZURE_CONNECTION_STRING=DefaultEndpointsProtocol=https;AccountName=YOURACCOUNTNAME;AccountKey=YOURACCOUNTKEY

or for more advanced usage, see http://blogs.msdn.com/b/partlycloudy/archive/2009/12/08/configuring-the-storage-client-with-connection-strings.aspx, for example:

SET AZURE_CONNECTION_STRING=TableEndpoint=https://YOURACCOUNTNAME.TABLE.COM/;QueueEndpoint=https://YOURACCOUNTNAME.QUEUE.COM/;BlobEndpoint=https://YOURACCOUNTNAME.BLOB.COM/;AccountName=YOURACCOUNTNAME;AccountKey=YOURACCOUNTKEY

You can optionally set environment variables for TIMEOUT (in seconds) and RETRY_COUNT - particulalrly useful if you are on a slow connection.


Examples
--------

	ListContainers

	ListBlobs

	ListBlobs mycontainer

	PutBlob myfilename mycontainer

	PutBlob myfilename mycontainer/myblob

	GetBlob mycontainer/myblob

	DeleteBlob mycontainer/myblob

	CopyBlob mycontainer/myblob1 mycontainer/myblob2

	ListQueues

	ListTables


Rob Blackwell

November 2010