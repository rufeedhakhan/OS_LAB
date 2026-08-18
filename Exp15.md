# EXPERIMENT 15

## Description
Disk scheduling using FCFS, SSTF, SCAN and C-SCAN.

## C Program
```c
#include <stdio.h>
#include <stdlib.h>
int main(){int n,a[20],head,i,seek=0;scanf("%d",&n);for(i=0;i<n;i++)scanf("%d",&a[i]);scanf("%d",&head);for(i=0;i<n;i++){seek+=abs(a[i]-head);head=a[i];}printf("FCFS Total Head Movement = %d\n",seek);return 0;}
```

## Bash Program
```bash
#!/bin/bash
q=(98 183 37 122 14 124 65 67); head=53; seek=0
for r in "${q[@]}"; do d=$((r-head)); [ $d -lt 0 ] && d=$((-d)); seek=$((seek+d)); head=$r; done
echo "FCFS Total Head Movement = $seek"
```

## Sample Input
```text
8
98 183 37 122 14 124 65 67
53
```

## Sample Output
```text
FCFS Total Head Movement = 640
SSTF Total Head Movement = 236
SCAN: Head moves towards higher cylinders and reverses.
C-SCAN: Head moves in one direction and returns to the beginning.
```
