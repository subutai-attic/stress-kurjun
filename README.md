# stress-kurjun
JMeter configuration for stressing kurjun

## Prepare test environment

1. Download [JMeter](http://jmeter.apache.org/)
2. Copy jars in libs/ folder to $JMETER_HOME/lib
3. Start JMeter and open "Stress Kurjun2.jmx" file
4. Set Kurjun instance configuration in "User Defined Variables" (host, port, protocol)
    * host - ip address/domain name of kurjun
    * port - service port
    * protocol - service protocol (http/https)
5. Enable tests that you need (by righ click > Enable), start stress (CTRL + R)
6. By setting properties for Thread Groups you can define stress weight against service
    * Number of Threads - number of requests sent indenpendently (used to simulate concurrent connections to server)
    * Ramp-Up Period - time period between each thread to start after another
    * Loop Count - indicate how many times thread is repeated
