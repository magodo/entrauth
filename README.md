# Intro

`entrauth` provides a customizable chained token credential for authenticating to Microsoft Entra ID.

The high level structure of supported credentials are listed below:

```
Auth
  |
  +--> OAuth2 Client Credential
  |      |
  |      +------ client secret ----------------------> "client-secret"
  |      |
  |      +------ client assertion
  |                    |
  |                    +----- plain assertion -------> "assertion-plain" 
  |                    |
  |                    +----- assertion file --------> "assertion-file" 
  |                    |
  |                    +----- client certificate ----> "client-certificate" 
  |                    |       (build assertion)
  |                    |
  |                    +------ request --------------> "assertion-request"
  |                                                    (Github, AzureDevOps)
  +--> Token Provider
         |
         +------ Azure Managed Identity -------------> "managed-identity"
         |
         +------ Azure CLI delegation ---------------> "azure-cli"
         |
         +------ Azure Developer CLI delegation -----> "azure-dev-cli"
```
