Ansible static site deploy
=============================

## Example

``` yaml
- hosts: localhost
  remote_user: user
  roles:
    - {
        role: static-deploy,
        deploy_to: "/srv/www/static-deploy", # required
        deploy_from: "dest", # by default directory build
        keep_releases: 3, # by default 5
        linked_sample_files: [ 'babel_settings.js', 'config/secrets.js' ], # by default empty array
        sample_extname: 'example' # by default sample
      }
```
