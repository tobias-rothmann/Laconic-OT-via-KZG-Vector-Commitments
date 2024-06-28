# Laconic-OT-via-KZG-Vector-Commitments

Fleischhacker, Hall-Andersen, and Simkin recently published a [paper](https://eprint.iacr.org/2024/264.pdf) on constructing efficient laconic oblivious transfer using the KZG as a vector commitment scheme. Altough their OT scheme is not more efficient than state-of-the-art OT schemes for exchanging single OT instances, it outperforms every state-of-the-art OT scheme in the laconic i.e. batched case. Due to the homomorphic property of KZG commitments, mutiple OT instances can be added homorphically to one single KZG commitment, which is the main reason for the efficiency boost.

## Preliminaries
Before diving into the concrete costruction proposed by Fleischhacker et al. we first need to understand what it is that they achived. 
In this part we briefly discuss what (laconic) oblivious transfer, the KZG, and vector commitments are.

### Oblivious Transfer
Oblivious Transfer (OT) is a cryptograophic primitive widely used in multi-party computation (MPC). 
OT is a two party interactive protocol between Alice and Bob. Essentially it allows Alice to give Bob a choice of two messages m0, m1, such that Bob can only choose to receive one of them (either $m0$ or $m1$) and furthermore Alice cannot know which one Bob chose. 
Laconic OT is basically a batched version of OT, it allows Alice and Bob to exchange lists of messages $[(m0,m1), (m2,m3),...]$ and choices $[b0,b1,...]$ in a OT manner i.e. per list entry $i$ Bob can only receive one message ($m2i$ or $m2i+1$) and Alice cannot know which message from the list entry Bob chose ($bi$).


### KZG
The KZG is a polynomial commitment scheme. Essentially, it allows a party to commit to a polynomial and later on reveal points of the polynomial without revealing the polynomial it self. 




### Vector Commitments
