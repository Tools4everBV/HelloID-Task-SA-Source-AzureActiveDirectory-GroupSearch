# HelloID-Task-SA-Source-AzureActiveDirectory-GroupSearch

## Prerequisites
- [ ] This script uses the Microsoft Graph API and requires an App Registration with App permissions:
  - [ ] Read all groups <b><i>Group.Read.All</i></b>

## Description

1. Define a wildcard search query `$searchQuery` based on the search parameter `$datasource.searchGroup`
2. Creates a token to connect to the Graph API.
3. List all groups in Azure AD using the API call: [List groups](https://learn.microsoft.com/en-us/graph/api/group-list?view=graph-rest-1.0&tabs=http)
4. Filter down to only users with `$searchQuery` in their `displayName` or `userPrincipalName`
5. Return a hash table for each user account using the `Write-Output` cmdlet.

> To view an example of the data source output, please refer to the JSON code pasted below.

```json
{
    "searchGroup": "Group A"
}
```