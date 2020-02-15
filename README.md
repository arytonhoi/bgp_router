Our initial high-level approach was to represent our forwarding table as a dictionary, 
in which the key was the first three "chunks" of an IP address we could receive as one to send
messages to and the value was the IP address(es) that we should send to as a result. 
This made most of the implementation more straightfoward since we could look up where to send messages to in our forwarding table.

However, this became a challenge that we faced when it came to aggregation. To fix this, we created a "predump" in our dump function.
This allowed us to add back the ".0" to the network before we did the aggregation.

We tested our code by including a lot of clear print statements so that we could see what was happening whenever we ran our code.
It was especially helpful to print out variables that we were setting to ensure that they were getting set as we intended.
