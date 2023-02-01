# go-port-scanner (gps)
A simple pocket sized port scanner written in Go.

# Why?
The idea dawned on me when I was solving a HTB machine where you needed to perform a port scan to discover internal networks while running proxychains. So, you either needed a portable `nmap` binary (found one, but didn't work) or an alternate method. I could not find any simple tool to just upload it to the remote machine and scan ports. There were `ps1` and `batch` scripts, but they were not straight forward to use.

So, here we are. A simple, portable, easy to use port scanner. Also, I wanted to do something with Go.

___Note: This is not as efficient as `nmap` and it does not aim to replace `nmap`. This tool's purpose is to be your emergency port scanner when you don't have access to `nmap`.___

# How to use?

```text
go run gps.go

-i    IP address to scan. Default is localhost.
-t    Number of threads to use for scanner. The input values get divided accordingly and each thread gets equal number of ports to scan. Default is 20.
-v    Verbose output (currently kinda useless and I used it to debug). If true, shows failed connections too. Default is false.
-d    Delay/Timeout time for each connection in milliseconds. Default is 700ms.
-p    Ports to scan. Default value (empty field) scan will use nmap top 1000 ports.
      Custom ports example: 21,22,53,... etc.
-h    Displays these options.
```

# TODO
- Add port range scans
- Clean the code and make it more readable (currently looks like a rushed job (which it was))
- Add pre-built Linux and Windows binaries
- Research on how to improve the performance more. (Maybe apply some of them OOP patterns?)
- Add UDP maybe?
- Colors?

When? Later.
