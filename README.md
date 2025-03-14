# FLECS Create Repository Action
A GitHub action to create new repositories

# Usage
## Minimal example
```yml
uses: FLECS-Technologies/create-repository-action@v1
with:
  name: "repository-name"
  org: "organization"
env:
  GITHUB_TOKEN: "access token with with repo admin permission"
```
## Advanced example
```yml
uses: FLECS-Technologies/create-repository-action@v1.x
with:
  name: "repository-name"
  org: "organization"
  description: "description"
  private: false
  auto-init: false
  gitignore-template: "Rust"
  license-template: "Apache-2.0"
env:
  GITHUB_TOKEN: "access token with with repo admin permission"
```

# Inputs
| Name               | Description                       | Example                      | Required | Default |
| ------------------ | --------------------------------- | ---------------------------- | -------- | ------- |
| name               | Name of the new repository        | "awesome-project"            | Yes      | -       |
| org                | GitHub organization               | "FLECS-Technologies"         | Yes      | -       |
| description        | Description of the new repository | "Contains only awesome code" | No       | -       |
| private            | Visibility of the new repository  | true                         | No       | false   |
| auto-init          | Create commit with empty README   | true                         | No       | false   |
| gitignore-template | Create .gitignore from template   | true                         | No       | false   |
| license-template   | Create LICENSE from template      | "Rust"                       | No       | -       |

See [GitHub REST API documentation](https://docs.github.com/en/rest/repos/repos?apiVersion=2022-11-28#create-an-organization-repository) for further examples and explanation.

# Environment
| Name         | Description                                                                                                       | Required |
| ------------ | ----------------------------------------------------------------------------------------------------------------- | ---------|
| GITHUB_TOKEN | A GitHub access token or GitHub Apps installastion token with the "Administration" repository permissions (write) | true     |

# License
[Apache 2.0](https://github.com/FLECS-Technologies/create-repository-action/blob/v1.x/LICENSE)
