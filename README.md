gh-prop
---

Manage repository custom properties

Requirements:

Your GitHub token will need to have the appropriate scopes to manage repository custom properties.
You will need following scopes:
- `repo`
- `read:org`

In order to set a property you will need to have owner permissions on the repository.

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
````
