# utilites

- [x] `wcat`
- [ ] `wgrep`
- [ ] `wzip`
- [ ] `wnuzip`



## `wcat`

**Details:**

- Your program **wcat** can be invoked with one or more files on the command line; it should just print out each file in turn. 
- In all non-error cases, **wcat** should exit with status code 0, usually by returning a 0 from **main()** (or by calling **exit(0)**).
- If *no files* are specified on the command line, **wcat** should just exit and return 0. Note that this is slightly different than the behavior of normal UNIX **cat** (if you'd like to, figure out the difference).
- If the program tries to **fopen()** a file and fails, it should print the exact message "wcat: cannot open file" (followed by a newline) and exit with status code 1. If multiple files are specified on the command line, the files should be printed out in order until the end of the file list is reached or an error opening a file is reached (at which point the error message is printed and **wcat** exits).

### Syscall

`fopen` 

```c
FILE* *fopen(const char *pathname, const char *mode)
```



`fgets()`

```c
char *fgets(char *str, int n, FILE *stream)
```

```c
//example
#define MAX_WORDS 1<<10
char buffer[MAX_WORDS];
fgets(buffer, MAX_WORDS, stdin);
printf("%s", buffer);
```

通过这样基本的函数就可以完成把标准输入（输入到屏幕里的命令）存储到buffer里的工作然后能输出。

如果要完成这里的任务，那么我们就要调整标准输入为我们想要的文件作为输入，也就是要用`fopen()`取得这个时候`FILE`定义的`fp`就起作用了。（File这个数据结构是什么可以自行查阅）



`fclose()`

获取完一份文件中的内容后，不要忘记要关闭文件

`perror`

系统错误

`strerror`

返回一个描述错误代码的字符串

> The strerror() function returns a pointer to a string that describes the error code
> passed in the argument errnum, possibly using the LC_MESSAGES part of  the  current
> locale  to select the appropriate language.  (For example, if errnum is EINVAL, the
> returned description will be "Invalid argument".)  This string must not be modified
> by  the application, but may be modified by a subsequent call to strerror() or str‐
> error_l().  No other  library  function,  including  perror(3),  will  modify  this
> string.

### function & variables

`File` is a opaque data type, but it's a struct defined.

```c
FILE *fp = fopen("main.c", "r");
if (fp == NULL){
  printf("cannot open file\n");
  exit(1);
}
```

**Q:** What is FILE, like `FILE *fp1, fp2`

You could find answer in [this](https://www.geeksforgeeks.org/data-type-file-c/)

Definition of FILE is in `stdio`, although it is system specific.

`buffer` 缓存读取的文件内容

### Source code

```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
 
#define MAX_WORDS 1<<10
 
int main(int argc, char* argv[]){
    FILE *fp;
    char buffer[MAX_WORDS];
    memset(buffer, 0x00, MAX_WORDS); //initial array
 
    // if no command exists, then exit
    if(argc == 0 && argc == 1){
        exit(0);
        return 0;
    }
 
    for(int i = 1; i < argc; ++i){
        fp = fopen(argv[i], "r");
        if(fp == NULL){
            printf("wcat: cannot open file\n");// notice the 6.out has a space between  "wcat:" and "cannot"
            exit(1);
        }
        while((fgets(buffer, MAX_WORDS, fp))!= NULL）{
            printf("%s", buffer);
        }
        fclose(fp);
    }
    return 0;
}
```



### Autotest and result

- Autotest instructions see the README.md 

- Result :

  ![image-20270323230322293](../../../../../../Library/Application%20Support/typora-user-images/image-20270323230322293.png)
