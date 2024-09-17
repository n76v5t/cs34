java c
COMP 9121 Week 2
Data-Link Layer
Exercise 1. CRC
(1) Consider the following information bits 1010101 and CRC generator 1101. What are the coded bits to be transmitted? Show that the coded bits are divisible by 1101.
(2) The system can be shown in the following figure.

Received bits – (minus) coded bits is called the error pattern (note that here “–” is equivalent to XOR). Obviously, all “0” error pattern means “no error”.
Please show
(a) Error pattern 0000100 can be detected by the receiver.
Not divisible by 1101
(b) Error pattern 0001101 cannot be detected by the receiver.
Divisible by 1101
(c) Could you find another error pattern which cannot be detected by the receiver?
0011010, 0110100, 1101000, so on.
Exercise 2. Slotted ALOHA
Consider two nodes, A and B, that use the slotted ALOHA protocol to contend for a channel. Suppose node A has more data to transmit than node B, and node A’s retransmission probability pA is greater than node B’s retransmission probability, pB.
(1) Provide a formula for node A’s average throughput. What is the total efficiency of the protocol with these two nodes?
(2) If pA= 2pB, is node A’s average throughput twice as large as that of node B? Why or why not? If not, how can you choose pA and pB to make that happen?
(3) In general, suppose there are N nodes, among which node A has retransmission probability 2p and all other nodes have retransmission probability p. Provide expressions to compute the average throughputs of node A and of any other node.
a) A’s average throughput is given by pA(1-pB). Total efficiency is pA(1-pB) + pB(1-pA).
b) A’s throughput is pA(1-pB)=2pB(1-pB)= 2pB- 2(pB)2. B’s throughput is pB(1-pA)=pB(1-2pB)= pB-2(pB)2. Clearly, A’s throughput is n代 写COMP 9121 Week 2  Data-Link LayerProlog
代做程序编程语言ot twice as large as B’s. In order to make pA(1-pB)= 2 pB(1-pA), we need that pA= 2 – (pA / pB).
c) A’s throughput is 2p(1-p)N-1, and any other node has throughput p(1-p)N-2(1-2p).
Exercise 3. More on Slotted ALOHA
Suppose four active nodes—nodes A, B, C and D—are competing for access to a channel using slotted ALOHA. Assume each node has an infinite number of packets to send. Each node attempts to transmit in each slot with probability p. The first slot is numbered slot 1, the second slot is numbered slot 2, and so on.
(1) What is the probability that node A succeeds for the first time in slot 5?
(2) What is the probability that some node (either A, B, C or D) succeeds in slot 4?
(3) What is the probability that the first success occurs in slot 3?
(4) What is the efficiency of this four-node system?
a) (1 – p(A))4 p(A) where, p(A) = probability that A succeeds in a slot p(A) = p(A transmits and B does not and C does not and D does not) = p(A transmits) p(B does not transmit) p(C does not transmit) p(D does not transmit) = p(1 – p) (1 – p)(1-p) = p(1 – p)3 Hence, p(A succeeds for first time in slot 5) = (1 – p(A))4 p(A) = (1 – p(1 – p)3)4 p(1 – p)3
b) p(A succeeds in slot 4) = p(1-p)3 p(B succeeds in slot 4) = p(1-p)3 p(C succeeds in slot 4) = p(1-p)3 p(D succeeds in slot 4) = p(1-p)3 p(either A or B or C or D succeeds in slot 4) = 4 p(1-p)3 (because these events are mutually exclusive)
c) p(some node succeeds in a slot) = 4 p(1-p)3 p(no node succeeds in a slot) = 1 - 4 p(1-p)3 Hence, p(first success occurs in slot 3) = p(no node succeeds in first 2 slots) p(some node succeeds in 3rd slot) = (1 - 4 p(1-p)3)2 4 p(1-p)3
d) efficiency = p(success in a slot) =4 p(1-p)3





         
加QQ：99515681  WX：codinghelp
