### ceph-deepscrubber

pawadski@gmail.com, apawel.me @ 2018

ceph-deepscrubber is a very simple tool that enables you to queue X amount of deep scrubs per pool

## Install

1. Clone the repository:   
`git clone https://gitlab.com/pawadski/ceph-deepscrubber /opt/deepscrubber`

2. Edit the config file:   
`nano /opt/deepscrubber/config`

Done. You can invoke it however often you want with a cronjob:
```
MAILTO=""
*/30 * * * * /opt/deepscrubber/deepscrubber
```

## Debugging

The debug flag argument `debug` will print more detailed log messages. If you're using syslog you will need to check syslog for output, with file logging output is printed to stdout.