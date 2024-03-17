# bulkCreateCvAzureObject
Use Commvault Rest API to create Azure Object backups for multiple Azure Storage Accounts

- This script will create a credential and instance for Azure File and Azure Blob in Commvault using the REST API
- The script will read from a csv file called input_object.csv
- The csv file should be in the same directory as the script
- The csv file should have the following columns: **name**, **key**, **servicePrincipal**. name is the storage account name, key is the storage account key, and servicePrincipal is the name of the service principal credential in Commvault
- The script will loop through each line in the csv file and create a credential for file and instance for Azure File and Azure Blob
- The script will use a pre-existing service principal cred for blob. It should exist already in Commvault
- The script will output a log file in the same directory as the script
- Need to set the `$planName`, `$commserve`, and `$accessNodes` variables.
- Domain user credentials should be in format `username@domain`
