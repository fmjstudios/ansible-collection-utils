# Ansible Role: Users

This role ensures that servers have a _sudo_ group, enables _sudo_ privileges for group members, creates a specified user and adds said user to the _sudo_ group. Lastly a new SSH public key is copied to the _authorized keys_ enabling the newly created user to access the server with his private key.

## Requirements

N/A

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
users:
  - app-runner
  - backup-runner
password: $6$rounds=4096$delta4x4$pFGL0fLrtWSjH0UWmEPJOvJvSSsO374c7YncGymHSnFBT98/xG3LFf29DY768n8zH3sZHMxlG5JEHXTbASxW9.
```

## Dependencies

None.

## Example Playbook

```yaml
    - hosts: all
      roles:
        - role: user
```

## License

Proprietary

## Author Information

This role was created in 2023 by [Maximilian Gindorfer](https://fmj.dev).
