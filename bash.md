Bash
====

Use "strict" mode.

- `set -o errexit` (or `set -e`) Exit on error
- `set -o pipefail` If pipefail is  enabled, the  pipeline's return status is the value of the last (rightmost)
   command to exit with a non-zero status, or zero if all commands exit successfully. (quote from man bash) 
- `set -o nounset` (or `set -u`) Raises error on use uninitialized variables.

Start your bash script with code below for "strict mode".

```
set -o errexit
set -o pipefail
set -o nounset
```

Sources

- [Best Practices for Writing Bash Scripts](https://kvz.io/bash-best-practices.html)
- [set -e, -u, -o, -x pipefail explanation](https://gist.github.com/mohanpedala/1e2ff5661761d3abd0385e8223e16425)
- man bash

