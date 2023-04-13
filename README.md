# LoRa Uplink/Downlink Monitoring

I am working on a radio controlled drone/robot project. For the radio communication I am using [LoRa](https://de.wikipedia.org/wiki/Long_Range_Wide_Area_Network#LoRa_Allianz) in a [peer-to-peer configuration](https://de.wikipedia.org/wiki/Peer-to-Peer).
The downside of Lora is that its communication is connection-less, ergo you cannot ensure that a transmission has been received accordingly.
In my case, this would be if the drone goes out of range or the radio communication is disrupted otherwise.

To mittigate this problem, I have invented an novel light weight algorithm heavily inspirerd by vector [clock alrogithm](https://en.wikipedia.org/wiki/Vector_clock) and [heart beat algorithm](https://en.wikipedia.org/wiki/Heartbeat_(computing)).
It basically a stateless fire-and-forget ping pong to exchange incrementing numbers.
Thus allowing monitoring of uplink and downlink the radio communication to detect a lost link.
