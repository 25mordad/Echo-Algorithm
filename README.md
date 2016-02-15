# Echo algorithm
The echo algorithm is a centralized wave algorithm for undirected networks. The initiator starts by sending a message to all its neighbors. Intuitively, these messages travel in all directions, and bounce back from the corners of the network toward the initiator. This is achieved as follows. When a noninitiator receives a message for the first time, it makes the sender its parent, and sends a message to all neighbors except its parent. When a noninitiator has received messages from all its neighbors, it sends a message to its parent. Finally, when the initiator has received
messages from all its neighbors, it decides.
- Distributed Algorithms by Wan Fokkink-Page24

# configuration file:
- First line is the name of root for example: 127.0.0.1:8082, it means the ip address is 127.0.0.1 and the port is 8082
- After first line you should write the neighbor in each line with ip and port for example if the node has two neighbors, we write down:
127.0.0.1:8083
127.0.0.1:8084
- If the node is initiator, we should write: initiator:[nodeIP]:[nodePort], for example: initiator:127.0.0.1:8082

# node
How can I add a node?
- Just copy the node folder and rename it to what you want. Then change the configuration file as you need.
- All node files (node.go) are the same.

#Graph for Sample:
	87 --------- 86 ---------- 82 -------- 83
				 |			   |  
				 |			   |   
				 85            |
				 | \          / \
				 |  \        /   \
				 |   \      /     \
				 |    \    /       \
				 |     \  /         \
				 88 --- 84 -------- 81
