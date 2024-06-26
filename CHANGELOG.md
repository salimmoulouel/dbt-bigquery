# dbt-bigquery Changelog

- This file provides a full account of all changes to `dbt-bigquery`.
- Changes are listed under the (pre)release in which they first appear. Subsequent releases include changes from previous releases.
- "Breaking changes" listed under a version may require action from end users or external maintainers when upgrading to that version.
- Do not edit this file directly. This file is auto-generated using [changie](https://github.com/miniscruff/changie). For details on how to document a change, see [the contributing guide](https://github.com/dbt-labs/dbt-bigquery/blob/main/CONTRIBUTING.md#adding-changelog-entry)

## dbt-bigquery 1.8.0-b2 - April 03, 2024

### Features

- Add new workflow for internal patch releases ([#38](https://github.com/dbt-labs/dbt-bigquery/issues/38))

### Fixes

- remove `keyfile` from `_connection_keys` ([#1146](https://github.com/dbt-labs/dbt-bigquery/issues/1146))
- Add `pandas` extra for `google-cloud-bigquery` to pick up missing `pyarrow` dependency ([#1152](https://github.com/dbt-labs/dbt-bigquery/issues/1152))

### Under the Hood

- Add unit test for transaction semantics. ([#1123](https://github.com/dbt-labs/dbt-bigquery/issues/1123))

### Dependencies

- hard pin ddtrace to 2.3.0 ([#1141](https://github.com/dbt-labs/dbt-bigquery/pull/1141))
- Add `dbt-core` as a dependency to preserve backwards compatibility for installation ([#1168](https://github.com/dbt-labs/dbt-bigquery/pull/1168))

### Security

- Pin `black>=24.3` in `dev-requirements.txt` ([#1151](https://github.com/dbt-labs/dbt-bigquery/pull/1151))



## dbt-bigquery 1.8.0-b1 - March 01, 2024

### Features

- Add support for checking table-last-modified by metadata ([#938](https://github.com/dbt-labs/dbt-bigquery/issues/938))
- Support limiting get_catalog by object name ([#950](https://github.com/dbt-labs/dbt-bigquery/issues/950))
- Update base adapter references as part of decoupling migration ([#1067](https://github.com/dbt-labs/dbt-bigquery/issues/1067))
- Support all types for unit testing in dbt-bigquery, expand coverage of safe_cast macro ([#1090](https://github.com/dbt-labs/dbt-bigquery/issues/1090))

### Fixes

- Patch for json inline --show ([#972](https://github.com/dbt-labs/dbt-bigquery/issues/972))
- Lower bound of `2.11.0` for `google-api-core` ([#979](https://github.com/dbt-labs/dbt-bigquery/issues/979))
- Fix refresh syntax, config comparison with empty labels ([#983](https://github.com/dbt-labs/dbt-bigquery/issues/983))
- Assign the correct relation type to materialized views in catalog queries ([#995](https://github.com/dbt-labs/dbt-bigquery/issues/995))
- Fix inline comments (--) on the last line of an incremental model ([#896](https://github.com/dbt-labs/dbt-bigquery/issues/896))
- In incremental models, add dummy merge condition on source partition column when partition is required ([#792](https://github.com/dbt-labs/dbt-bigquery/issues/792))
- Support agate Integer type, test with empty seed ([#1003](https://github.com/dbt-labs/dbt-bigquery/issues/1003))
- Fixed issue where materialized views were failing on re-run with minimal config parameters ([#1007](https://github.com/dbt-labs/dbt-bigquery/issues/1007))
- Fix broken partition config granularity and batch_id being set to None ([#1006](https://github.com/dbt-labs/dbt-bigquery/issues/1006))
- replace deterministic batch_id with uuid ([#1006](https://github.com/dbt-labs/dbt-bigquery/issues/1006))
- remove json patch to leverage bigquery-python improvement ([#1055](https://github.com/dbt-labs/dbt-bigquery/issues/1055))
- remove `token` field from connection keys ([#1105](https://github.com/dbt-labs/dbt-bigquery/issues/1105))
- Remove custom query job async timeout logic as it has been fixed in bigquery-python ([#1081](https://github.com/dbt-labs/dbt-bigquery/issues/1081))

### Under the Hood

- Upgrade spark-bigquery Java deps for serverless to 2.13-0.34.0 ([#1006](https://github.com/dbt-labs/dbt-bigquery/issues/1006))
- Primary and foreign key constraints are not enforced in BigQuery ([#1018](https://github.com/dbt-labs/dbt-bigquery/issues/1018))
- Add tests for --empty flag ([#1029](https://github.com/dbt-labs/dbt-bigquery/issues/1029))
- Migrate to dbt-common and dbt-adapters package ([#1071](https://github.com/dbt-labs/dbt-bigquery/issues/1071))

### Dependencies

- Update ddtrace requirement from ~=1.19 to ~=1.20 ([#948](https://github.com/dbt-labs/dbt-bigquery/pull/948))
- Update pre-commit-hooks requirement from ~=4.4 to ~=4.5 ([#960](https://github.com/dbt-labs/dbt-bigquery/pull/960))
- Bump mypy from 1.5.1 to 1.6.0 ([#963](https://github.com/dbt-labs/dbt-bigquery/pull/963))
- Update pre-commit requirement from ~=3.4 to ~=3.5 ([#969](https://github.com/dbt-labs/dbt-bigquery/pull/969))
- Update black requirement from ~=23.9 to ~=23.10 ([#973](https://github.com/dbt-labs/dbt-bigquery/pull/973))
- Bump mypy from 1.6.0 to 1.6.1 ([#985](https://github.com/dbt-labs/dbt-bigquery/pull/985))
- Update ddtrace requirement from ~=1.20 to ~=2.1 ([#989](https://github.com/dbt-labs/dbt-bigquery/pull/989))
- Update black requirement from ~=23.10 to ~=23.11 ([#1013](https://github.com/dbt-labs/dbt-bigquery/pull/1013))
- Update pytest-xdist requirement from ~=3.3 to ~=3.4 ([#1022](https://github.com/dbt-labs/dbt-bigquery/pull/1022))
- Bump mypy from 1.6.1 to 1.7.0 ([#1023](https://github.com/dbt-labs/dbt-bigquery/pull/1023))
- Update ddtrace requirement from ~=2.1 to ~=2.2 ([#1028](https://github.com/dbt-labs/dbt-bigquery/pull/1028))
- Update wheel requirement from ~=0.41 to ~=0.42 ([#1033](https://github.com/dbt-labs/dbt-bigquery/pull/1033))
- Bump mypy from 1.7.0 to 1.7.1 ([#1034](https://github.com/dbt-labs/dbt-bigquery/pull/1034))
- Update ddtrace requirement from ~=2.2 to ~=2.3 ([#1035](https://github.com/dbt-labs/dbt-bigquery/pull/1035))
- Update pytest-xdist requirement from ~=3.4 to ~=3.5 ([#1037](https://github.com/dbt-labs/dbt-bigquery/pull/1037))
- Update freezegun requirement from ~=1.2 to ~=1.3 ([#1040](https://github.com/dbt-labs/dbt-bigquery/pull/1040))
- Update black requirement from ~=23.11 to ~=23.12 ([#1056](https://github.com/dbt-labs/dbt-bigquery/pull/1056))
- get dbt-tests-adapters from dbt-adapters repo ([#1077](https://github.com/dbt-labs/dbt-bigquery/pull/1077))

### Contributors
- [@gmyrianthous](https://github.com/gmyrianthous) ([#979](https://github.com/dbt-labs/dbt-bigquery/issues/979))
- [@matt-winkler](https://github.com/matt-winkler) ([#972](https://github.com/dbt-labs/dbt-bigquery/issues/972))
- [@tnk-ysk](https://github.com/tnk-ysk) ([#896](https://github.com/dbt-labs/dbt-bigquery/issues/896), [#792](https://github.com/dbt-labs/dbt-bigquery/issues/792))

## Previous Releases
For information on prior major and minor releases, see their changelogs:
- [1.6](https://github.com/dbt-labs/dbt-bigquery/blob/1.6.latest/CHANGELOG.md)
- [1.5](https://github.com/dbt-labs/dbt-bigquery/blob/1.5.latest/CHANGELOG.md)
- [1.4](https://github.com/dbt-labs/dbt-bigquery/blob/1.4.latest/CHANGELOG.md)
- [1.3](https://github.com/dbt-labs/dbt-bigquery/blob/1.3.latest/CHANGELOG.md)
- [1.2](https://github.com/dbt-labs/dbt-bigquery/blob/1.2.latest/CHANGELOG.md)
- [1.1](https://github.com/dbt-labs/dbt-bigquery/blob/1.1.latest/CHANGELOG.md)
- [1.0](https://github.com/dbt-labs/dbt-bigquery/blob/1.0.latest/CHANGELOG.md)
