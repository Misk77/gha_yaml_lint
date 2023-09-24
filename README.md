[![GitHub Super-Linter](https://github.com/Misk77/gha_yaml_lint/actions/workflows/syntax-check.yml/badge.svg)](https://github.com/marketplace/actions/super-linter)

### Testing gha yamlint
# gha_yaml_lint


GitHub Action Super-Linter



E.g code:
- name: "Run validation"
        uses: docker://ghcr.io/github/super-linter:slim-v4.8.5
        env:
          DEFAULT_BRANCH: main
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          FILTER_REGEX_INCLUDE:
          FILTER_REGEX_EXCLUDE:
          VALIDATE_ALL_CODEBASE: false
          VALIDATE_YAML: true
          VALIDATE_ANSIBLE: true
          VALIDATE_BASH: true
          VALIDATE_PYTHON: true



NOTES:
All VALIDATE [LANGUAGE]: is set to true as default  
If you set a specific LANGUAGE to be validate, all other lagague will be set to false = they will not be lint and need to be specific specified  
VALIDATE_ALL_CODEBASE:  
- Here we can choose if whole repo should be lint all the time
VALIDATE_ALL_CODEBASE:
  -  true  = default all repo will always be lint
VALIDATE_ALL_CODEBASE:
  - false = Will only lint new or edited files for each run
FILTER_REGEX_INCLUDE:
If set, , t it will only check directory or files that is set as values
Default - If not set, the default is, all,  if will include whole repo
ANSIBLE_CONFIG_FILE:
If you want to set your own rules for yaml lint
E.g
> ansible-lint  --config-file=/home/misk/FTP/Github/gha/gha_yaml_lint/.github/workflows/TEMPLATES/.ansible-lint.yml  ansible/ansible-code.yaml






Source:

https://github.com/marketplace/actions/super-linter


ANSIBLE-lint


> ansible-lint --generate-ignore  --config-file=/home/misk/FTP/Github/gha/gha_yaml_lint/.github/workflows/TEMPLATES/.ansible-lint.yml  ansible/ansible-code.yaml

Create a ignore file that can be used:  .ansible-lint-ignore
