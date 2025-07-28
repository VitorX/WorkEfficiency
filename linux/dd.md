# Convert and Copy a File

## below is the sample to check the value of memory location
1. Write a simple program to show the addres of virable **i** like:
    ```
    //byteorder.c
    #include <stdio.h>
    #include <stdlib.h>

    int main(int argc,char **argv)
    {
        int i=0x01020304;
        int *p=&i;
        char *c=(void *)p;
        printf("%p\n",&i);
        printf("%p\n",&p[0]);
        printf("%p\n",&p[1]);
        printf("%p\n",&p[2]);
        printf("%p\n",&p[3]);
        printf("0x%x\n",i);
        printf("%d,%d,%d,%d\n",c[0],c[1],c[2],c[3]);
       
        printf("%p\n",&i);
        printf("%ld\n",&i);
        getchar();
        return 0;
    }

    ```
1. Run the program and get the address of variable:i
    0x7fffffffdd54
    0x7fffffffdd54
    0x7fffffffdd58
    0x7fffffffdd5c
    0x7fffffffdd60
    0x1020304
    4,3,2,1
    **0x7fffffffdd54**
    **140737488346452**
1. Get the process id of this program using **pgrep** command
    ```
    $ pgrep byte
    67742
    ```
1. Cacluate the decimal value of the pointer address:0x7fffffffdd54
    140,737,488,346,452
1. Using dd command to print the vaule of this process's memory locaion at 0x7fffffffdd54
    ```
    $ sudo dd bs=1 skip="140737488346452" count=1024 if="/proc/67742/mem" status=none | hexdump -C
    
    00000000  04 03 02 01 54 dd ff ff  ff 7f 00 00 54 dd ff ff  |....T.......T...|
    00000010  ff 7f 00 00 00 45 5e 9e  31 6e 04 a4 01 00 00 00  |.....E^.1n......|
    00000020  00 00 00 00 90 9d c2 f7  ff 7f 00 00 00 00 00 00  |................|
    00000030  00 00 00 00 89 51 55 55  55 55 00 00 70 de ff ff  |.....QUUUU..p...|
    ```

