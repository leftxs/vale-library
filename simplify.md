```yaml
-rw-r--r--    1 svx staff     86 Mar 15 12:05 yarn.lock
# Checks for sentences where e.g. "perform validation" can be simplified to "validate".
extends: existence
ignorecase: true
message: "'%s': Try simplifying this by omitting the first word and turning the last word into a verb."
level: suggestion
tokens:
  - (?:(perform|do|run)\w*( \w+)* \w+(tions?|ing))
This catches all of these:
performing validation (=validate)
running the installation (=install)
run testing (=test)
do testing (=test)
```