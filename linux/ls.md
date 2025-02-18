# ls

## list the file types by exclude exe file type
 ls --ignore=*.exe|sed -E 's/[a-zA-Z0-9]+\./\./g'|sort|uniq