a. AMQP stands for Advanced Message Queuing Protocol. It is an open standard application layer protocol for message-oriented middleware, which enables different applications or components to communicate by passing messages between them.

b. In the context of "guest:guest@localhost:5672":

"guest" is the username used to authenticate with the AMQP server.
"guest" is also the password associated with the username.
"localhost:5672" refers to the hostname and port of the AMQP server. "localhost" indicates that the server is running on the local machine, and "5672" is the default port number used by AMQP for communication.

c. Simulation slow subscriber
![image](https://github.com/Samuelwidjaja/tutorial8-subscriber/assets/119392779/0570ecf6-5640-479d-8b1c-060723f48187)
Total number queue dalam mesin saya adalah 30, karena saya melakukan `cargo run` Publisher sebanyak 8 kali.

d. Reflection and Running at least three subscribers
![image](https://github.com/Samuelwidjaja/tutorial8-subscriber/assets/119392779/26bed66a-672c-4244-accd-319ad277df70)
When I tried running three subscriber consoles at the same time, each one ended up handling different events because the tasks got split among them.

![image](https://github.com/Samuelwidjaja/tutorial8-subscriber/assets/119392779/615e6dfa-f580-465f-9195-35ee0c42d655)
In the graph shown, there's a noticeable change compared to when I used only one console. The number of queued messages has decreased. This occurred because messages are now being consumed concurrently by three subscribers. Consequently, this reduces the number of queued messages and enhances the speed of message consumption.

