# Hashseq

**what problem does it solve**

a. logos is an open network

a. existing sequence CRDTs assume honeset participants. they are easily corrupted.

**what makes hashseq different**

a. an unbounded number of anonymous editors

a. uncorruptable and fault-tolerant: no trust in any clock or actor id

a. documents, lists and records, not only strings

a. fast enough to be invisible

what is a CRDT — ppl searching this out already know what it is\
CRDT: Conflict-Free Replicated Data Type (CRDT)



A Byzantine-Fault-Tolerant (BFT) CRDT family for unpermissioned networks with an unbounded number of collaborators. This crate implements the **HashWeb** design: content-addressed ops with self-certifying BLAKE3 ids, an explicit causal hash-DAG, and one design law — _state is a pure function of the op set; every order-sensitive decision resolves at read time_.





