# diary_c

## vscode terminal 乱码

```json
    // "terminal.integrated.shellArgs.windows": ["/K chcp 65001 >nul"],
    "terminal.integrated.shellArgs.windows": ["-NoExit", "/c", "chcp 65001"],
    "terminal.integrated.fontFamily": "Lucida Console",
```

## print struct 规范

```c

#include <stdio.h>
#include <string.h>

typedef struct MyC_St
{
    char a[50];
    char author[50];
    char subject[100];
    int book_id;
} MyC;

void print_MyC(MyC book);

int main()
{
    MyC Book1;

    strcpy(Book1.title, "C Programming");
    strcpy(Book1.author, "xyz");
    strcpy(Book1.subject, "Programming");
    Book1.book_id = 123456;

    print_MyC(Book1);
}

// 打印结构体规范
void print_MyC(MyC myc)
{
    printf("\n\r print_MyC ([book_id]: %d )：\n",myc.book_id);
    printf(">  title : %s\n", myc.title);
    printf(">  author : %s\n", myc.author);
    printf(">  subject : %s\n", myc.subject);
    printf("\n\r");
}

```
