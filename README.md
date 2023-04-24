# multi-clients-chat-application
Multiple clients-server chat application built in java swing. It supports message delivery to the offline clients and vector clock implementation, based on https://github.com/ankitrathore25/multi-clients-chat-application

The project contains 3 main files. 
- ServerView.java - It contains code for server. This class must be run first.
- loginClient.java - It contains code for client's login and run after the server has been started. It can be run as many number of times depending upon number of clients required.
- ClientView.java - It contains code for the client.

A client can send message to offline client too. I have used activemq (messaging queue) to implement this feature.

Steps to Run:
- Download activemq in your computer. Start activemq at local server using command line. Just open cmd/terminal and navigate to the bin folder of the downloaded activemq and run the command `start activemq`.
- Now you can check the queues on the UI of activemq. You can check out other videos on youtube on how to use activemq.
- Start the server first.
- Create as many client as you want by running the client class.

To implement offline client messaging. Send all the messages to the activemq first and then fetching from there to send it to the intended clients.

`Assumption` : when a client comes online again then it will first check the message using 'check messages' button before sending or receiving any message.

References:
https://www.youtube.com/watch?v=rd272SCl-XE
https://www.youtube.com/watch?v=ZzZeteJGncY
