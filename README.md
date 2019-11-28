---
page_type: sample
languages:
- csharp
products:
- azure
- azure-storage
- dotnet-core
description: "How to upload and download blobs from Azure Blob Storage with .NET."
urlFragment: upload-download-blobs-net
---

# How to upload and download blobs from Azure Blob Storage with .NET

## Azure SDK Versions
To use the previous Azure SDK version [azure-sdk-for-net-storage-blob-upload-download-v11], please add the following dependency:
- [Microsoft.Azure.Storage.Blob]

For the latest Azure SDK version [azure-sdk-for-net-storage-blob-upload-download-v12], please add the following dependency: 
- [Azure.Storage.Blobs]

## Prerequisites

To complete this tutorial:

* Install .NET Core latest version for [Linux] or [Windows]

If you don't have an Azure subscription, create a [free account] before you begin.

### Create a Storage Account using the Azure Portal

Step 1 : Create a new general-purpose Storage Account to use for this tutorial.
 
*  Go to the [Azure Portal] and log in using your Azure account. 
*  Select **New** > **Storage** > **Storage account**. 
*  Select your Subscription. 
*  For `Resource group`, create a new one and give it a unique name. 
*  Enter a name for your storage Account.
*  Select the `Location` to use for your Storage Account.
*  Set `Account kind` to **StorageV2(general purpose v2)**.
*  Set `Performance` to **Standard**. 
*  Set `Replication` to **Locally-redundant storage (LRS)**.
*  Set `Secure transfer required` to **Disabled**.
*  Check **Review + create** and click **Create** to create your Storage Account. 
 
Step 2 : Copy and save Connection string.

After your Storage Account is created. Click on it to open it. 
Select **Settings** > **Access keys** > **Key1/key**, copy the associated **Connection string** to the clipboard, then paste it into a text editor for later use.

### Put the connection string in an environment variable

This solution requires a connection string be stored in an environment variable securely on the machine running the sample. Follow one of the examples below depending on your operating system to create the environment variable. If using Windows close your open IDE or shell and restart it to be able to read the environment variable.

Linux

```bash
export AZURE_STORAGE_CONNECTIONSTRING="<YourConnectionString>"
```

Windows

```cmd
setx AZURE_STORAGE_CONNECTIONSTRING "<YourConnectionString>"
```

At this point, you can run this application. It creates its own file to upload and download, and then cleans up after itself by deleting everything at the end.

## Run the application
First, clone the repository on your machine:

```bash
git clone https://github.com/Azure-Samples/storage-blobs-dotnet-quickstart.git
```

Then, switch to the appropriate folder:

Navigate to your directory where the project file (.csproj) resides and run the application with the `dotnet run` command.

```console
dotnet run
```

## This sample shows how to do following operations of Storage Blobs
- Create a Storage Account using the Azure Portal.
- Create a container.
- Upload a file to block blob.
- List blobs.
- Download a blob to file.
- Delete a blob.
- Delete the container.

## More information

The [Azure Storage documentation] includes a rich set of tutorials and conceptual articles, which serve as a good complement to the samples.

This project has adopted the [Microsoft Open Source Code of Conduct].
For more information see the [Code of Conduct FAQ] or contact [opencode@microsoft.com] with any additional questions or comments.

<!-- LINKS -->
[azure-sdk-for-net-storage-blob-upload-download-v11]: https://github.com/Azure-Samples/azure-sdk-for-net-storage-blob-upload-download/tree/master/azure-sdk-for-net-storage-blob-upload-download-v11
[Microsoft.Azure.Storage.Blob]: https://www.nuget.org/packages/Microsoft.Azure.Storage.Blob/
[azure-sdk-for-net-storage-blob-upload-download-v12]: https://github.com/Azure-Samples/azure-sdk-for-net-storage-blob-upload-download/tree/master/azure-sdk-for-net-storage-blob-upload-download-v12
[Azure.Storage.Blobs]: https://www.nuget.org/packages/Azure.Storage.Blobs/
[Linux]: https://dotnet.microsoft.com/download
[Windows]: https://dotnet.microsoft.com/download
[free account]: https://azure.microsoft.com/free/?WT.mc_id=A261C142F
[Azure Portal]: https://portal.azure.com
[Azure Storage documentation]: https://docs.microsoft.com/azure/storage/
[Microsoft Open Source Code of Conduct]: https://opensource.microsoft.com/codeofconduct/
[Code of Conduct FAQ]: https://opensource.microsoft.com/codeofconduct/faq/
[opencode@microsoft.com]: mailto:opencode@microsoft.com