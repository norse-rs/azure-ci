
<h1 align="center">azure-ci</h1>
<p align="center">
    <a href="https://github.com/norse-rs">
       <img src="https://img.shields.io/badge/project-norse-9cf.svg?style=flat-square" alt="NORSE">
    </a>
</p>

Small collection of Azure Pipelines scripts for use in Rust projects.

## Example

Running rustfmt, clippy and tests on the repository:

```yaml
stages:
 - stage: Lint
   jobs:
     - template: job-fmt.yaml@templates
     - template: job-clippy.yaml@templates
 - stage: Test
   jobs:
     - template: job-test.yaml@templates

resources:
  repositories:
    - repository: templates
      type: github
      name: norse-rs/azure-ci
      endpoint: <ENDPOINT>
```
