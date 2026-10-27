---
icon: rocket-launch
---

# Getting started

**HashSeq is a sequence CRDT designed to represent and modify a sequence in a distributed environment.**

HashSeq gives operations a way to identify specific items and describe relationships between them. This allows multiple participants to make changes independently and later merge those changes into a consistent sequence.

At a high level, HashSeq represents the sequence as a graph of relationships between items. The graph records information about where items belong and how operations affect those relationships. HashSeq can then use that information to determine the resulting sequence.



* key concepts
* architecture&#x20;



{% hint style="info" %}
If you're evaluating the platform for your team rather than yourself, jump to [Core concepts](https://app.gitbook.com/s/H05NL9dvOiK5q1pSLVf5/core-concepts "mention") first — it'll save time when you set things up properly.
{% endhint %}

