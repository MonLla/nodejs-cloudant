# 2.0.3 (UNRELEASED)

# 2.0.2 (2018-02-14)
- [FIXED] Updated `require` references to use newly scoped package
  `@cloudant/cloudant`.

# 2.0.1 (2018-02-14)
- [NEW] Added API for upcoming IBM Cloud Identity and Access Management support
  for Cloudant on IBM Cloud. Note: IAM API key support is not yet enabled in the
  service.
- [NEW] Support multiple plugins.
  _See [api-migration.md](https://github.com/cloudant/nodejs-cloudant/blob/master/api-migration.md)
  for migration details._
- [NEW] Allow use of a custom service name from the CloudFoundry VCAP_SERVICES
  environment variable.
- [FIXED] Fix `get_security`/`set_security` asymmetry.
- [FIXED] Support piping of request payload with plugins.
- [BREAKING CHANGE] Replace `retryAttempts` option with `maxAttempts`. This
  defines the maximum number of times the request will be attempted.
- [BREAKING CHANGE] By default the `retry` plugin will retry requests on HTTP
  429 status codes, a subset of 5xx server error status codes and also TCP/IP
  errors.
  _See [api-migration.md](https://github.com/cloudant/nodejs-cloudant/blob/master/api-migration.md)
  for migration details._
- [BREAKING CHANGE] Changed `promise` plugin to throw new `CloudantError` (not
  `string`).
- [REMOVED] Remove global `retryTimeout` option (replaced by plugin specific
  configuration).
- [REMOVED] Remove previously deprecated method `set_permissions`.
- [IMPROVED] Updated documentation by replacing deprecated Cloudant links with
  the latest bluemix.net links.

# 1.10.0 (2017-11-01)
- [UPGRADED] Upgrade package: cloudant-nano@6.7.0.

# 1.9.0 (2017-10-20)
- [NEW] Add 'error' & 'response' events to 429 retry plugin stream.
- [FIXED] `{silent: true}` to dotenv to prevent `.env` warnings.
- [UPGRADED] Upgrade package: cloudant-nano@6.6.0.
- [UPGRADED] Upgrade package: debug@^3.1.0.
- [UPGRADED] Upgrade package: request@^2.81.0.

# 1.8.0 (2017-05-23)
- [UPGRADED] Using cloudant-nano==6.5.0 dependancy.
