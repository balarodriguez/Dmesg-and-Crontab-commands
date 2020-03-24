# Dmesg-and-Crontab-commands


dmesg commands

#!/usr/bin/env bash

dmesg | tail -5 > demsg3.txt
grep -w "usecs" demsg3.txt
grep -i "usecs" demsg3.txt
grep -c "usecs" demsg3.txt
grep -cw "usecs" demsg3.txt


crontab commands 

1) background process

#!/usr/bin/env bash


sleep 500

echo "hello world"

crontab command to monitor cpu and mem utilisation and uploading the details
2)#!/usr/bin/env bash

top -b -n 2 -d 0.2 -p 7356 | tail -1 | awk '{print $9"\t"$10}' >> bg_output.txt
