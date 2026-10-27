---
icon: book
---

# Core concepts

* **Operations** — describe changes made to the sequence.
* **Nodes** — represent items and their relationships in the HashSeq graph.
* **Payloads** — contain the value associated with an inserted item.
* **References (`refs`)** — identify other nodes that an operation observes or refers to.
* **Anchors** — identify where an insertion or move should be placed.
* **Targets** — identify the item an operation acts upon.
* **Overwrites** — replace an existing relationship with a new one.
* **Placement** — determines where items appear in the resulting sequence.
* **Liveness** — determines which items are currently present in the sequence.



*   Operations

    * Insert — adds a new item to the sequence.
      *   An insert identifies an **anchor**, which describes where the new item should be placed relative to an existing item.

          For example, consider the sequence:

          ```
          A → B → C
          ```

          An operation can insert `D` relative to `B`:

          ```
          A → B → D → C
          ```

          The important part is that the operation refers to an existing item rather than relying on a numeric position such as "index 2."

          An insert also contains a **payload**. The payload is the value being inserted into the sequence.

          For example:

          ```
          payload = "bobby likes cake"
          ```

          The payload is the content of the new item. It is not itself a reference to another item in the sequence.
    * Remove — removes an existing item from the sequence.
      *   A remove operation identifies an existing item that should no longer appear in the sequence.

          The item being removed is the operation's **target**.

          For example:

          ```
          A → B → C
          ```

          A remove operation targeting `B` results in:

          ```
          A → C
          ```

          The target therefore answers the question:

          > **Which existing item is this operation acting on?**
    * Move — changes the position of an existing item.
      *

          A move operation changes the position of an existing item.

          A move needs to identify both:

          1. the **target** — the item being moved
          2. the **anchor** — the item that determines where the target is moved

          For example:

          ```
          A → B → C → D
          ```

          If `C` is moved relative to `A`, the resulting sequence might be:

          ```
          A → C → B → D
          ```

          Here:

          * `C` is the **target** because it is the item being moved.
          * `A` is the **anchor** because it determines the new placement.

          This distinction is useful throughout HashSeq:

          > **The target identifies what an operation acts on. The anchor identifies where something should be placed.**




* Anchors
* References
  * observed frontier
  * honest construction
  * named references
* Resources
* Conflict resolution



* Elements
* Gaps
* Liveness
* Placemet
* Concurrent operations

***

### The mental model in 30 seconds

You sign up and get an **account**. Your account belongs to one or more **workspaces**. Each workspace contains **projects**. Members are invited to a workspace and given a role; that role determines what they can do across all projects in that workspace.

That's it — the rest is detail.
