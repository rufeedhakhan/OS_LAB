# EXPERIMENT 14

## Description
File allocation strategies: Sequential, Indexed, and Linked allocation.

## C Program
```c
#include <stdio.h>
int main(){int n,b[20],i;scanf("%d",&n);for(i=0;i<n;i++)scanf("%d",&b[i]);printf("Linked Allocation: ");for(i=0;i<n;i++){printf("%d",b[i]);if(i<n-1)printf(" -> ");}printf(" -> NULL\n");return 0;}
```

## Bash Program
```bash
#!/bin/bash
read -p "Number of blocks: " n
read -a b
echo -n "Linked Allocation: "
for ((i=0;i<n;i++)); do echo -n "${b[i]}"; [ $i -lt $((n-1)) ] && echo -n " -> "; done
echo " -> NULL"
```

## Sample Input
```text
5
5 9 13 17 20
```

## Sample Output
```text
Linked Allocation: 5 -> 9 -> 13 -> 17 -> 20 -> NULL
```
