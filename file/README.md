# 7Z

## search text file type in a zip folder
    >7z l -r C:\Users\v-feixue1\Desktop\b.zip *.txt

# Find the files by exclude specific file type

## list the file types by exclude exe file type
 ls --ignore=*.exe|sed -E 's/[a-zA-Z0-9]+\./\./g'|sort|uniq
