# ku-latency
an example to use SO_TIMESTAMP, come from https://vilimpoc.org/research/ku-latency/
-----
usage:

Compiles clean (or should) with:

gcc -o ku-latency ku-latency.c -lrt -Wall

gcc -o send-data send-data.c -lrt -Wall

Usage looks like this:

    Usage: ./ku-latency [-i IP address] [-p port]

           -h          Help.
           -i          Specifies IP address of interface you want to listen to.
           -e          Specifies the ethernet interface name you want to listen to.
           -p          Specifies port number of packets you want to see.

    If neither option is specified (they are both optional), then the program
    will listen on IPADDR_ANY (all interfaces), port 1025.
    ~$ ./send-data
    Not all * required parameters were entered.

    ./send-data accepts the following parameters: 

            * --destination or -d [ip address]
              --port        or -p [port number]          (default: 1025)
              --repeat      or -r [repeat every x msec.] (default: 20)
To do the measurements, pop open two Terminal windows and have one run the ku-latency listener and the other run the send-data packet sender.
