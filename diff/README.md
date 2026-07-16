# Purpose
To convert unified diffs into html for local and easy review

# Usage
```bash
# create recursive unified diff then convert to html
# note: you will need to update the code if you use anything other than "diff -ru"
% diff -ru metadata-templates metadata.azure.prod | ~/src/RudiBob/code-reading/diff/cvsweb.cgi -d > /tmp/diff.html
% open /tmp/diff.html
```