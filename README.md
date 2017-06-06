# loadbalancing-my-way

    Description

HAProxy, which stands for High Availability Proxy, is a popular open source software TCP/HTTP Load Balancer and proxying solution. But the client connections stays with haproxy. When there are millions of connections we do not want to scale up on haproxy nodes ( as client connects to it) but rather use it as just loadbalancer but then let the client connections stay with the application itself which if it is already designed and offers to support those large number of concurrent connections.

    Who are you targeting and how are you enhancing their experience?

many teams own and manage their application through haproxy. in some similar scenarios this solution can fit in and benefit them. avoids the need to worry on haproxy scaling concerns and instead utilize and enjoy their application capabilities.

    What is your solution?

solution is to let haproxy first loadbalance but when connection reaches backend application then redirect to itself. This will make client connections to terminate on haproxy and connect to the application and still achieves loadbalancing across the backend application.

    What makes this idea better than what already exists?

we dont have to scale immensely at all at haproxy level but still utilize its loadbalancing capabilities and on the other hand we can immensely utilize the applications' scaling capabilities.

    Do you have any data/research that supports your idea?

yes i have a setup where it was applied and tested.

    What results do you hope to achieve?

haproxy to loadbalance but hold minimal connections. All client connections to stay with the actual backend application.

    What skill sets are required to develop your idea?

haproxy, tcp/ip, http/https, ws, wss
