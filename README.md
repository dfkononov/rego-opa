# OPA Policies

A starter repository for OPA Policies. Proposed repository structure contains:
* policies - policy files written in Rego language. Policy might have several files:
  * *policy.rego* - policy definition;
  * *policy.meta.rego* - additional policy metadata which contains violation description, severity, type etc.;
  * *policy_tests.rego* - unit tests for policy;
* *.manifest* - metadata file having the following sections:
  * *root* - standard OPA element which allows loading mutiple bundles;
  * *policies* - non-standard element, which will be processed by custom execution engine. 

## Testing

To run tests locally use:
```
opa test --bundle ./ --verbose --format pretty
```
