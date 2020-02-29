# Frequent IPs Counter
### co-author: [Marina Angelovska](https://github.com/marinaangelovska)

# Description
With the help of a socket network traffic simulator written in Java, it has been decided to develop a simple Spark Streaming application to process and monitor TCP-based tuples consisting of a _port + ip_address_. A Spark Streaming function called _countByValueAndWindow_  has been used to filter the occurrences of the tuples in a certain time window and above a certain threshold.


## How to run
Run the java helper to simulate the network traffic and after that run the pyspark class to monitor and count. In order to run the script, the following bash-command was used:
`spark-submit frequent ips.py < host > < port > < min packets > < window >`


## Results
With the following command `spark-submit frequent ips.py localhost 9999 5 30`, the script listens to the port 9999 on localhost, it sets 5 to the min packets variable and it counts in a window of 30 seconds. The following pictures show two subsequent time windows:

![First time window](https://github.com/dadadima94/spark-streaming-frequent-ips/blob/master/images/result1.png)

![Second time window](https://github.com/dadadima94/spark-streaming-frequent-ips/blob/master/images/result2.png)


