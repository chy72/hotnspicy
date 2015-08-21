# hotnspicy
TCP/IP Assignment with Dr Anang

<h1> Group Member </h1>
1112702444 Ahmad Saifuddin
1112700661 Kok Pin Zong


<h2> Task That Have Been Carried Out </h2>
1. Create Github Account and Install Git
2. launch Git Bash
3. Moving to Folders
4. Create Folder and File
5. Git Respitory
6. Status Update
7. Staging
8. Committing
9. updating Git about Github
10. A Push or A Shove

<h2>Work Distribution</h2>
All work distribution are equally divided among members

<h2>codes<h2/>


```c++
#include <stdio.h>
#include <string.h>

int main(int argc, const char * argv[])
{
    FILE *fp;

    char returnData[64];

    fp = popen("/sbin/ifconfig eth0", "r");

    while (fgets(returnData, 63, fp) != NULL)
    {
        if (returnData[0] == '\n') {
            continue;
        }

        char no1[60], no2[60];
        strcpy(no1, strtok(returnData, " "));
    if (strcmp("inet", no1) != 0) {
            continue;
        }

        strcpy(no2, strtok(NULL, " "));
        printf("%s %s\n", no1, no2);

    }

    return 0;
}

```
