# Changelog

## 2.0.0

Fork of `diablomedia/zendframework1-auth-adapter-dbtable`, published as `gizmocraft/zendframework1-auth-adapter-dbtable`.

### Breaking changes

- Requires PHP `>=8.5`. Tested on PHP 8.5 and 8.6.
- Package renamed from `diablomedia/zendframework1-auth-adapter-dbtable` to `gizmocraft/zendframework1-auth-adapter-dbtable`. It now requires `gizmocraft/zendframework1-auth` `^2.0.0` and `gizmocraft/zendframework1-db` `^2.0.0`.

### Other changes

- PHP 8.6: `setAmbiguityIdentity()` uses `is_int()` instead of the deprecated `is_integer()`. No signature changes.
- Dev dependencies upgraded (PHPUnit 13, PHPStan 2.3, php-cs-fixer 3.95, GrumPHP 2.27). Dropped `composer-require-checker`, which has no release for PHP 8.6.
- Tests migrated to PHPUnit 13 attributes. `phpunit.xml.dist` references `phpunit-bootstrap.php` again (upstream dropped it in 1.0.8, so the SQLite tests were never enabled on CI); `tearDown()` no longer fails when `setUp()` skipped the test. The SQLite tests run when `GITHUB_ACTIONS` is set or `TESTS_ZEND_AUTH_ADAPTER_DBTABLE_PDO_SQLITE_ENABLED` is defined.
- CI runs PHP 8.5 and 8.6.
