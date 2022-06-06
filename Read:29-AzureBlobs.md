# Read: 29 - Azure Blobs

- Azure Blob storage is Microsoft's object storage solution for the cloud.  
- Blob storage is optimized for storing massive amounts of unstructured data.  
- Unstructured data is data that doesn't adhere to a particular data model or definition, such as text or binary data.  
- Blob storage is designed for:  
     - Serving images or documents directly to a browser.  
     - Storing files for distributed access.  
     - Streaming video and audio.  
     - Writing to log files.  
     - Storing data for backup and restore, disaster recovery, and archiving.  
     - Storing data for analysis by an on-premises or Azure-hosted service.  

- Blob storage resources : Blob storage offers three types of resources:
     - The storage account  
     - A container in the storage account  
     - A blob in a container  
     - 
- Storage accounts : 

      - provides a unique namespace in Azure for your data.  
      - Every object that you store in Azure Storage has an address that includes your unique account name.  
      - The combination of the account name and the Blob Storage endpoint forms the base address for the objects in your storage account.  

- Blobs : Azure Storage supports three types of blobs:
     - Block blobs store text and binary data. Block blobs are made up of blocks of data that can be managed individually. Block blobs can store up to about 190.7 TiB.  
     - Append blobs are made up of blocks like block blobs, but are optimized for append operations. Append blobs are ideal for scenarios such as logging data from virtual machines.  
     - Page blobs store random access files up to 8 TiB in size. Page blobs store virtual hard drive (VHD) files and serve as disks for Azure virtual machines. For more information about page blobs, see Overview of Azure page blobs  

## Quickstart: Azure Blob Storage client library v12 for .NET
- Setting up => Azure Blob Storage client library v12 for .NET.
- Create the project  
     1- create a new console app with the name BlobQuickstartV12 => dotnet new console -n BlobQuickstartV12   
     2- Switch to the newly created BlobQuickstartV12 directory. => cd BlobQuickstartV12   
     3- create another directory called data. => mkdir data   
     
- Install the package  
dotnet add package Azure.Storage.Blobs 

- Set up the app framework
   1- Open the Program.cs file in your editor.    
   2- Remove the Console.WriteLine("Hello World!"); statement.    
   3- Add using directives.    
   4- Update the Main method declaration to support async.    
- Copy your credentials from the Azure portal.    
- Configure your storage connection string.    
- Restart programs.  
   

