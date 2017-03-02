Ansible static site deploy
=============================

## Example

```
- hosts: localhost
  remote_user: user
  roles:
    - {
        role: static-deploy,
        application: "my-application",
        deploy_from: "dist", # by default directory dist
        keep_releases: 3, # by default 5
        linked_sample_files: [ 'babel_settings.js', 'config/secrets.js' ], # by default empty array
        sample_extname: 'example' # by default sample
      }
```
