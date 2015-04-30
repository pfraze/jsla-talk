

class: center, middle, inverse

# Decentralized Databases
### and the End of the Web Host

---

class: center, middle

# Secure Scuttlebutt

[github.com/ssbc](github.com/ssbc)

## Paul Frazee

@pfrazee

---

class: center, middle

# The Web is not FOSS

---

class: middle

.centerblock[
# The Web is not FOSS

### Deployments are closed and proprietary.

- Users cannot audit the services.
- Users can't access their data in its raw form.
- Users can't push changes.
]

---

class: center, middle

# Self-hosting doesn't solve this

The Web is not created equal.

The networks are not open to third parties.

User saturation **matters**.

---

class: center, middle

# The result: users lose 

No freedom to innovate.

No meaningful policing.

No community self-policing.

**Minority control.**

---

class: middle

<blockquote>
  <p>The big thing about distributed source control is that it makes one of the main issues with SCM's go away - <strong>the politics around "who can make changes."</strong> [BitKeeper] showed that you can avoid that by just giving everybody their own source repository.</p>
  <p>&mdash; <a href="http://www.linux.com/news/featured-blogs/185-jennifer-cloer/821541-10-years-of-git-an-interview-with-git-creator-linus-torvalds">Linus Torvalds</a></p>
</blockquote>

---

class: center, middle

# Single-Authority SCM

All commits go to a single host.

--

## Why?

Solves complex questions about concurrent changes.

---

class: center, middle

# Distributed-Authority SCM

Users clone the repo and work locally, no central authority.

--

## How?

Content hashing, keypair signatures, smarter merging

---

class: center, middle

## Can this principle be re-applied?

---

class: center, middle

<blockquote>
  The big thing about <strong style="font-size: 21px">distributed source control</strong> is that it makes one of the main issues with SCM's go away - the politics around "who can make changes." [BitKeeper] showed that you can avoid that <strong style="font-size: 21px">by just giving everybody their own source repository</strong>.
  &mdash; <a href="http://www.linux.com/news/featured-blogs/185-jennifer-cloer/821541-10-years-of-git-an-interview-with-git-creator-linus-torvalds">Linus Torvalds</a>
</blockquote>

---

class: center, middle

# Distributed <strike style="color: #808080">Source Control</strike> Web Services

**Their own <strike style="color: #808080">Source Repository</strike> Deployments**

---

class: center, middle

# Secure Scuttlebutt

The Web without hosts.

---

class: padded, middle

# Overview

--

- Users publish JSON feeds

--

- Feeds are followed socially

--

- Sync occurs in the background

---

class: center, middle

# Users publish JSON feeds

No restriction on schema.

---

class: center, middle

# Feeds are followed socially

Like Twitter or RSS.

---

class: center, middle

# Sync occurs in the background

Gossip protocol over LAN and Internet.

---

class: center, middle

# Gossip is highly cached

Nodes rehost messages for each other.

Connections are transitive.

---

class: center, middle

# Some users are Public

The **"Pub"** nodes.

Not special, just reachable on the net (domain name optional)

Usually bots, provide high availability.

---

class: middle

.centerblock[
# Overview

- Users publish JSON feeds

- Feeds are followed socially

- Sync occurs in the background

<br><br>
]

---

class: middle, padded

# Protocol Guarantees

--

- Monotonic Progress

--

- Provable Authorship

--

- History Can Not Be Changed


---

class: center, middle

# Monotonic Progress

Only one feed mutation: add.

User feeds are not shared so there's no chance of conflict.

---

class: center, middle

# Provable Authorship

All feeds have a keypair.

First message, <code>init</code>: publish the public key.

All messages are signed.

---

class: center, middle

# History Can Not Be Changed <small>(1/2)</small>

Each message includes the content-hash of the previous message.

---

class: center, middle

# History Can Not Be Changed <small>(2/2)</small>

Trying to alter history makes the hashes stop agreeing, and you stop getting gossiped.

**Change your history, and you're forked.**

---

class: middle, padded

# Overview

- Users publish JSON feeds
- Feeds are followed socially
- Sync occurs in the background

# Protocol Guarantees

- Monotonic Progress
- Provable Authorship
- History Can Not Be Changed

---

class: center, middle

# Conventions

---

class: center, middle

# Messages are typed

A string of any value.

---

class: center, middle

# Links are Content Hashes

Feed Links: content hash of the pubkey.

Message Links: content hash of the message.

Blob Links: content hash of the blob.

---

class: middle, padded

# Overview

- Users publish JSON feeds
- Feeds are followed socially
- Sync occurs in the background

# Protocol Guarantees

- Monotonic Progress
- Provable Authorship
- History Can Not Be Changed

# Conventions

- Messages are typed
- Links are content hashes

---

class: center, middle

# Demo

---

class: middle, padded

# Thank you!

@pfrazee

github.com/ssbc

# Further Discussion

- Applications

- Web of Trust

- End to End Encryption