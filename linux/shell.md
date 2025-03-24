## Input last commands's arguments
If the previous command had two arguments, like this `ls a.txt b.txt`

    # giving a.txt
    !:1
    # giving a.txt b.txt
    !:1-2

## Get Last commands's return value
    $?