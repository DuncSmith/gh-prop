gh-prop
---

Manage repository [custom properties](https://docs.github.com/en/organizations/managing-organization-settings/managing-custom-properties-for-repositories-in-your-organization)

Requirements:

Your GitHub token will need to have the appropriate scopes to manage repository custom properties.
You will need following scopes to read properties and the schema:
- `repo`
- `read:org`

And to set properties, you will need to be an org owner or have the `repository_custom_properties:write`

See the API docs for more information

- https://docs.github.com/en/rest/repos/custom-properties?apiVersion=2022-11-28
- https://docs.github.com/en/rest/orgs/custom-properties?apiVersion=2022-11-28


````
Usage: gh prop <command> [options]

Manage repository custom properties

Commands:
  list        List properties for a repository
  set         Set a property for a repository
  schema      Get the schema for an organization
  search      Search for a matching property value in a repository

Options:
  -r <owner/repo>   Specify the owner and repository name
  -p <property>     The name of the property
  -v <value>        The value of the property

Examples:
  gh prop list
  gh prop list -r octocat/hello-world
  gh prop set -r octocat/hello-world -p Team -v "Team A"
  gh prop schema
  gh prop schema octocat
  gh prop search -v "Any value"
  gh prop search -p "Team" -v "Team A"
  gh prop search -r octocat/hello-world -p "Team" -v "Team A"
````
