# VS Code

Install [Visual Studio Code](https://code.visualstudio.com) and VS Code
extensions on Fedora.

## Role Variables

### defaults/main.yml

| name               | description                             | type | default |
| ------------------ | --------------------------------------- | ---- | ------- |
| vs_code_extensions | A list of VS Code extensions to install | List | []      |

### vars/main.yml

| name              | description           | type | default                                           |
| ----------------- | --------------------- | ---- | ------------------------------------------------- |
| microsoft_key_url | URL for Microsoft key | URL  | https://packages.microsoft.com/keys/microsoft.asc |

## Example Playbook

```yaml
- hosts: workstations
  tasks:
  - import_role:
      name: vscode
    vars:
      vs_code_extensions:
        - ms-python.python
        - rust-lang.rust
```

## License

MIT
