# Sort by column
## using head/tail to format the text then sort by column
    dumpbin /exports C:\Windows\System32\combase.dll |tail -n +20 |head -n -12|sort -k 3