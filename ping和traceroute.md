## 关于ping命令和traceroute的实验报告

## 实验一 

1. ping 192.168.1.1

   ```
   ping 192.168.1.1
   PING 192.168.1.1 (192.168.1.1): 56 data bytes
   Request timeout for icmp_seq 0
   Request timeout for icmp_seq 1
   Request timeout for icmp_seq 2
   Request timeout for icmp_seq 3
   ^C
   --- 192.168.1.1 ping statistics ---
   5 packets transmitted, 0 packets received, 100.0% packet loss
   ```

2. ping 127.0.0.1

   ```
   ping 127.0.0.1
   PING 127.0.0.1 (127.0.0.1): 56 data bytes
   64 bytes from 127.0.0.1: icmp_seq=0 ttl=64 time=0.054 ms
   64 bytes from 127.0.0.1: icmp_seq=1 ttl=64 time=0.100 ms
   64 bytes from 127.0.0.1: icmp_seq=2 ttl=64 time=0.119 ms
   64 bytes from 127.0.0.1: icmp_seq=3 ttl=64 time=0.072 ms
   ^C
   --- 127.0.0.1 ping statistics ---
   4 packets transmitted, 4 packets received, 0.0% packet loss
   round-trip min/avg/max/stddev = 0.054/0.086/0.119/0.025 ms
   ```

## 实验二

	(base)  xuchangqi@xuchangqideMacBook-Pro  ~   main  traceroute 127.0.0.1
	traceroute to 127.0.0.1 (127.0.0.1), 64 hops max, 52 byte packets
	 1  localhost (127.0.0.1)  0.344 ms  0.124 ms  0.105 ms
	 
	 
	 
	(base)  xuchangqi@xuchangqideMacBook-Pro  ~   main  traceroute 192.8.0.1
	traceroute to 192.8.0.1 (192.8.0.1), 64 hops max, 52 byte packets
	 1  10.133.255.254 (10.133.255.254)  17.666 ms  9.038 ms  9.611 ms
	 2  172.20.255.250 (172.20.255.250)  10.669 ms  10.159 ms  9.670 ms
	 3  172.20.255.254 (172.20.255.254)  9.417 ms  9.020 ms  9.542 ms
	 4  172.17.11.214 (172.17.11.214)  10.714 ms  10.302 ms  9.664 ms
	 5  172.17.11.254 (172.17.11.254)  9.434 ms  8.914 ms  9.724 ms
	 6  218.197.158.254 (218.197.158.254)  10.531 ms  9.060 ms  11.303 ms
	 
	 traceroute www.baidu.com
	traceroute: Warning: www.baidu.com has multiple addresses; using 14.215.177.39
	traceroute to www.a.shifen.com (14.215.177.39), 64 hops max, 52 byte packets
	 1  10.133.255.254 (10.133.255.254)  3.826 ms  3.312 ms  3.278 ms
	 2  172.20.255.250 (172.20.255.250)  3.125 ms  3.969 ms  3.985 ms
	 3  172.20.255.254 (172.20.255.254)  4.388 ms  4.207 ms  5.871 ms
	 4  172.18.1.250 (172.18.1.250)  3.162 ms  2.899 ms  5.945 ms
	 5  localhost (59.172.178.133)  98.977 ms  4.139 ms  3.008 ms
	 6  111.175.209.65 (111.175.209.65)  6.602 ms  7.209 ms  7.658 ms
	 7  111.175.225.65 (111.175.225.65)  4.374 ms  16.569 ms  4.331 ms
	 8  202.97.98.210 (202.97.98.210)  18.953 ms  18.505 ms
	    202.97.29.65 (202.97.29.65)  21.346 ms
	^C











