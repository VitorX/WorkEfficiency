# Find Command
## List file types in a directory recursively
    find . -type f -printf "%f\n"|sed -E 's/[_a-zA-Z0-9\-]+\./\./g'|sort|uniq|grep "\."

## Find files with mutiple extension
    find . -type f \( -iname "*.dll" -o -iname "*.exp" -o -iname "*.ilk"  -o -iname "*.lib" -o -iname "*.obj" -o -iname "*.pdb" \)


## Delete the files find by multiple extension
    find . -type f \( -iname "*.dll" -o -iname "*.exp" -o -iname "*.ilk"  -o -iname "*.lib" -o -iname "*.obj" -o -iname "*.pdb" \)  -delete

## Find the specific file with name
    find "C:\Windows\System32"  -type f -iname "ComCtl32.dll"