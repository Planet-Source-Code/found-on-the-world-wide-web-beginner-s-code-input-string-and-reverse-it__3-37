<div align="center">

## Beginner's Code: Input string and reverse it


</div>

### Description

Program inputs a string & prints it out backwards to a file.  Found at http://users.neca.com/jboxall/ja05002.htm
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Found on the World Wide Web](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/found-on-the-world-wide-web.md)
**Level**          |Beginner
**User Rating**    |4.0 (20 globes from 5 users)
**Compatibility**  |C, C\+\+ \(general\)
**Category**       |[Strings](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/strings__3-26.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/found-on-the-world-wide-web-beginner-s-code-input-string-and-reverse-it__3-37/archive/master.zip)





### Source Code

```
/* Jason Boxall 1/13/97 CSC 131 Lab#5              */
/* This program inputs a name(s) and prints it(them) out backwards */
#include <stdio.h>
#include <string.h>
FILE *fout;
void main()
{
  char name[20];
  char *getname();        /* Fuction prototype */
  void switcheroo(char *);    /* Fuction prototype */
  fout=fopen("a:lab5out.dat","w");
  strcpy(name,getname());
  while(strcmp("q",name))
  {
   switcheroo(name);
   fprintf(fout,"\n");
   strcpy(name,getname());
  }
}
char *getname()
{
  char name[20];
  printf("\n\nEnter in a name to print backwards or 'q' to quit: ");
  gets(name);
  return name;
}
void switcheroo(char *name)
{
  int x,i;
  x=strlen(name);
  for(i=(x-1);i>=0;--i)
   {
 putchar(name[i]);
    fprintf(fout,"%c",name[i]);
   }
}
```

