# <u>Lecture 1 Exercise 2</u> 

### Q: Computing End-to-End Delay
Consider the figure below with three links, each with the specified transmission rate and link length.
Assume the length of a packet is 16000^8 bits. The speed of light propagation delay on each link is 3 x 10<sup>8</sup> m/sec. 
![[Pasted image 20230127190806.png]]
#### <u>Given Information:</u>
Link 1's given ***transmission rate*** is 10 Mbps and Link Length is 3 km,
Link 2's given ***transmission rate*** is 1000 Mbps and Link Length 5000 km,
Link 3's given ***transmission rate*** is 10000 Mbps and Link Length 1 km.

### Questions to Answer:
1) What is the transmission delay of link 1? 
2) What is the propagation delay of link 1?
3) What is the total delay of link?
4) What is the transmission delay of link 2?
5) What is the propogation delay of link 2?
6) What is the total delay of link 2?
7) What is transmission delay of link 3?
8) What is the propogation delay of link 3?
9) What is total delay of link 3?
10) What is the total delay?

## <u>How to Approach Transmission Delay Problems.</u>
![[Pasted image 20230127212451.png]]
#### <u>Understanding Transmission Delay vs Propagation Delay</u>
The ***Transmission delay*** is the amount of time it takes to insert the entire packet of bits into the wire. 
* i.e. it's the time from when the first bit hits the wire until the last bit is transmitted.
The ***Propagation delay*** is the amount of time it takes any single bit to propagate (move/spread) across the wire.
* As soon as you begin transmission you'll start the timer, and you finish when the end of the bit makes it to the other end. 
	* Start at one end and end at the other. (It is **End-to-End**)
##### Sending a bit on a network is not instantaneous... it takes time
### An example of an equation:
![[Pasted image 20230127210307.png]]
#### <u>So how do you calculate this?</u>
(1) Take the stated Mbps transmission speed
(2) Divide it into the links per sec
Take a look at the equation written above in the handwritten notes.
If you have ***n Mbps*** multiplied by some number of seconds per meter so meter can cancel out and give you the right amount of time. 
* e.g. If it's 10 million bits per second and the link length is 3 **kilo**meters (3000 meters).

What you might want to do in this question is switch the transmission rate upside down. Which will end up as the following:![[Pasted image 20230127211714.png]]
#### The Bottom Line:
Understand what unit you're looking for when answering these questions.
* If you're looking for ***size*** your answer will be in ***bits***
* If you're looking for ***link length*** your answer will be in ***meters***
* If you're looking for either ***transmission delay*** or ***propagation delay*** it'll be in ***seconds***
###### Example searching for propagation delay:
So for example if you're looking for the **propagation delay**, you can take the ***size of the packet*** and divide it by the ***size per second***, you will end up with seconds.