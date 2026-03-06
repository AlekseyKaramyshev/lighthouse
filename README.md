
***

## Lighthouse Role README.md

**roles/lighthouse/README.md**
```markdown
# Lighthouse Role

Deploys VK Lighthouse monitoring dashboard with Nginx.

## Role Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `lighthouse_dir` | `/var/www/html/lighthouse` | Installation directory |
| `lighthouse_git_repo` | `https://github.com/VKCOM/lighthouse.git` | Git repository |
| `lighthouse_branch` | `master` | Git branch/tag |

## Requirements

- Debian/Ubuntu systems
- Git installed

## Example Playbook

```yaml
***
- hosts: lighthouse
  become: true
  vars:
    lighthouse_branch: "v1.2.0"
  roles:
    - role: lighthouse
