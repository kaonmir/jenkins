# Travis CI using NodeJS

## Concept of Travis CI

### Job Lifecycle

1. (OPTIONAL) Install `apt addons`
1. (OPTIONAL) Install `cache components`
1. `before_install`
1. `install`
1. `before_script`
1. `script`
1. (OPTIONAL) `before_cache` (iff caching is effective)
1. `after_success` or `after_failure`
1. (OPTIONAL) iff deployment is active
   1. `before_deploy` (iff deployment is active)
   1. `deploy`
   1. `after_deploy` (if deployment is active)
1. `after_script`
