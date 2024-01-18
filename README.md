usage: 

go-system-load.py [-h] [-c OCCU_RATE] [-p PERTIME] [-i INTERVAL] [-m--memory MEM] [-n NETINTERVAL]

optional arguments:

-h, --help show this help message and exit

-c , --occupancy cpu占用率

-p , --persistent 占用时长(秒)

-i , --interval 间隔调用(分)

-m , --memory 占用内存(MB)

-n , --netinterval 网络占用的时间间隔(分钟)

install：

sudo apt install speedtest-cli

sudo apt install pip

sudo apt install python3

sudo pip install argparse

sudo pip install cgroups

sudo pip install psutil

run:

cpu占用20%，每次占用10秒，每1分钟占用一次，长期占用内存100M，每2分钟跑一次speedtest：

nohup go-system-load.py -c 20 -p 10 -i 1 -m 100 -n 2 &

默认使用：

nohup go-system-load.py > /dev/null 2>&1 &
