---
layout: post
title:  "The Greatest Hits in Side Channel Attacks"
date:   2018-10-28 14:50:04 -0700
categories: security
---

### What are side channel attacks?

The idea behind "side channel" attacks is to use the physical effects caused by the execution of an algorithm to uncover information about a system. A side channel attack is different than a traditional security vulnerability in that traditional vulnerabilities expose bugs in the software itself.

#### The broad classes of side channel attacks

+ **Timing attacks** - exploit differences in the amount of time different operations take (examine a cheap/fast operation compared to an expensive/slow one).
+ **Power/electromagnetic/acoustic analysis** - exploit differences in the amount of power/electromagnetic radiation/sound consumed or produced by the computer to perform a certain operation. Similar to timing attacks, observing that a certain operation consumed a lot of power/produces a certain noise, in contrast to another low power/different sound signature operation.  
+ **Shared state** - exploit a shared cache (VM, cloud) to monitor access

#### Why is it cool?

Side channel attacks are often wild, off the wall ideas that don't seem possible at all. They often rely on a very simple (seemingly innocuous) piece of information being observed that ends up revealing much more than first meets the eye. The papers below describe techniques:

+ to detect what people are saying on Skype
+ to recover what people are saying in a room from just a video of a bag of potato chips present in the room
+ to recover information off of RAM after a laptop has been turned off
+ and more...

## The History of Side Channel Attacks

## 1996

The Paper: [Timing Attacks on Implementations of Diffie-Hellman, RSA, DSS, and Other Systems](https://www.paulkocher.com/doc/TimingAttacks.pdf)

One of the first papers to bring (theoretical) attention to the idea of using timing attacks to break cryptosystems. Provided the theoretical basis, but wasn't considered a pertinent concern at the time.

## 2001

The paper: [Timing Analysis of Keystrokes and Timing Attacks on SSH](https://people.eecs.berkeley.edu/~daw/papers/ssh-use01.pdf)

**Lesser known fact:**

+ It takes a different amount of time to type different key pair combinations on a keyboard
+ Each key press is sent over the network (not just when you're finished typing the password)

**The attack**:

+ The authors developed a side channel attack over ssh that is able to infer the passwords users type in from encrypted information sent over the network.
+ The authors developed statistical techniques that allowed them to infer the character sequences of passwords from the latency information they collected (they built a Hidden Markov Model (HMM) and developed a n-Viterbi algorithm for the keystroke sequence inference).
+ The authors were able to target users with shorter passwords, and drastically reduce the search space for passwords by monitoring the inter-keystroke timing events.


## 2003

The paper: [Remote Timing Attacks are Practical](https://crypto.stanford.edu/~dabo/papers/ssl-timing.pdf)

The first paper to show that timing attacks are of practical concern, and to suggest defense measures to prevent against them.
The authors devised a timing attack against OpenSSL. Their experiments show that it is possible to extract private keys from an OpenSSL-based web server running on a machine in the local network.

## 2005

The paper: [Cache-timing attacks on AES](https://cr.yp.to/antiforgery/cachetiming-20050414.pdf)

A lot of the cryptography that we use in 2018 is crypto that the author of this paper, Daniel J. Bernstein (DJB) came up with because he was the only person that focused on designing algorithms that people could write correctly.

People ended up using protocols that DJB came up with:

+ [ChaCha](https://cr.yp.to/chacha/chacha-20080128.pdf) - a common symmetric cipher
+ [ED25519](https://ed25519.cr.yp.to/) - a standard elliptic curve for elliptic curve cryptography

One of the first papers to bring up the theoretical considerations facing securing crypto against attacks.

+ The authors demonstrate complete AES key recovery from known-plaintext timings of a network server on another computer.


## 2007

The paper: [Blind TCP/IP hijacking is still alive](http://phrack.org/issues/64/13.html)

**Lesser known fact**:

+ The IP ID counter of the client is incremented when a reset packet is sent to the server.
+ The IP ID counter of the client stays the same if no reset packet is sent.

This fact is used by the authors to determine if their spoofed packet was successfully accepted by the victim.

**The attack**:
In [section 3](http://phrack.org/issues/64/13.html), the authors show how to determine the client's port, then the server's sequence number, and finally the client's sequence number (assuming the client's OS is a vulnerable OS).

## 2008

The paper: [Lest We Remember: Cold Boot Attacks on Encryption Keys](https://www.usenix.org/legacy/event/sec08/tech/full_papers/halderman/halderman.pdf)

<img src="/images/posts/coldboot2.jpg" height="auto" width="100%">

**Lesser known fact**

When we turn off our computers, we assume that everything stored in RAM goes away (but this doesn't happen instantaneously!).
RAM is a bunch of capacitors that lose charge according to some distribution, but it's not instantaneous.
You have a period after your machine shuts off where there is residual data in memory.
If you are using something like Bitlocker, your AES key for your hard drive is in memory somewhere, if you can pull that off you can find the decryption key is for your full disk encryption.

**The attack**:

Freeze chips to delay the RAM discharge!

Take a can of compressed air and empty it onto your memory chip in your laptop before you pull it out, you have ~ an hour before you lose 1% of the content on the RAM chip. You can pull off what the encryption keys are, and even if there is some noise, it's possible to fill in the gaps and find the encryption key. This is because of the way encryption keys are stored (there tends to be a lot of redundancy).

Take the RAM chip and throw it in liquid nitrogen and you have ~24 hours to pull off the data. Pull the frozen chip into another laptop, and search for an AES key in the RAM, or dump the entire chip to a USB stick.



## 2009

The paper: [Hey, You, Get Off of My Cloud…](https://hovav.net/ucsd/dist/cloudsec.pdf)

**Lesser known fact:**

+ It's possible to colocate your VM in Amazon's EC2 where you desire.

**The attack**:

+ The authors conducted a study on the infrastructure of Amazon's EC2 service and were able to identify and attack a target virtual machine (VM), by spawning new VM's until their VM was in proximity to their target VM.

+ The proximity to their target VM enabled the ability to launch side-channel attacks and obtain information about their target VM.
  + detect who their co-residents are
  + determine their rate of web traffic
  + timing attacks (keystrokes via ssh).

+ The authors demonstrate for the first time that shared caches allow an attacker to measure when other instances are under excessive load.

## 2010

The paper: [Uncovering Spoken Phrases in Encrypted Voice over IP Connections](http://www.cs.unc.edu/~fabian/papers/tissec2010.pdf)

<img src="/images/posts/skype.png" height="auto" width="100%">

**Lesser known fact:**

In the same way that some images compress better than others (an image that is half blue vs. a complex image with no clear repetitive patterns), some words and phrases (audio) compress better than others.

This fact is used by the authors to determine if chosen phrases were said or not during an encrypted Skype call.

**The attack**:

Analyzing Skype, the authors show that it is possible to detect certain phrases participants say even though the connection is encrypted based on timing and the audio compression. They demonstrate it is possible to detect:

+ whether someone says a target phrase with 50% accuracy
+ what language you are speaking (based on differences in hardness/consonants/compression)
+ the gender of the person speaking.

## 2012

The paper: [Cross-VM Side Channels and Their Use to Extract Private Keys](https://www.cs.unc.edu/~reiter/papers/2012/CCS.pdf)

<img src="/images/posts/vm.png" height="auto" width="100%">

**Lesser known fact:**

+ A very specific cipher text forces the CPU to do very expensive or cheap operations. This idea is used to trigger this specific performance trick.
Introduces a crypto attack that is an attack against a very specific performance advantage.

**The attack**:

+ "Through a novel combination of low-level systems implementation and sophisticated tools such as classifiers (e.g., SVMs and HMMs) and sequence
alignment algorithms, we assembled an attack that was sufficiently powerful to extract ElGamal decryption keys from a victim VM in our lab tests."



## 2013

The paper: [Practical Timing Side Channel Attacks Against Kernel Space ASLR](https://www.ieee-security.org/TC/SP2013/papers/4977a191.pdf)

<img src="/images/posts/userspace.png" height="auto" width="75%">

[Image Credit](https://drawings.jvns.ca/userspace/)

**Lesser known fact:**

+ Address Space Layout Randomization (ASLR) randomizes the space in memory where you keep libc and other things.
+ This is to prevent buffer overflow/control flow hijacking attacks.

**The attack**:

+ Paper shows that when you randomize the kernel space, that shows up differently in your CPU cache and you can de-randomize whatever the ASLR looks like for your kernel from user space.
+ Shared state: shared cache.
  + "We show that an adversary can implement a generic side channel attack against the memory management system to deduce information about the
  privileged address space layout. Our approach is based on the intrinsic property that the different caches are shared resources on computer systems."


## 2014

The paper: [The Visual Microphone: Passive Recovery of Sound from Video](http://people.csail.mit.edu/mrub/papers/VisualMic_SIGGRAPH2014.pdf)
<img src="/images/posts/chips.png" height="auto" width="100%">


**Lesser known fact**

+ Sound causes objects to vibrate!
+ A video of the minute vibrations of objects in a room (think a house plant, or a bag of potato chips) can be used to recover what was being said in the same room!

**The attack**:

+ "We show how, using only high-speed video of the object, we can extract those minute vibrations and partially recover
the sound that produced them"

### Watch [this video explanation](https://www.youtube.com/watch?v=FKXOucXB4a8). Seriously this is one of the coolest videos ever.




The paper: [RSA Key Extraction via Low-Bandwidth Acoustic Cryptanalysis](https://www.cs.tau.ac.il/~tromer/papers/acoustic-20131218.pdf)

**Lesser known fact**

+ Different operations use a different amount of power, put off a different amount of electromagnetic radiation.
+ Tends to be very low frequencies.

**The attack**:

+ Looks at the acoustic artifacts from a crypto operation. If you put a microphone next to a machine and send the exact right emails over and over again, you can expose the RSA key that GPG (program that implements PGP) is using to decrypt the email.


## 2018

The paper: [Off-Path TCP Exploit: How Wireless Routers Can Jeopardize Your Secrets](http://www.cs.ucr.edu/~zhiyunq/pub/sec18_TCP_offpath_wifi.pdf)

**Lesser known fact**

802.11 wifi is half duplex (two way communication, but only one direction at a time - not simultaneous - like a walkie-talkie, a phone call is "full duplex"), you can tell if a reset packet gets sent or not based on whether other communication going over wifi gets slowed down. If you as a wireless client detects that there is other traffic on your network, you do a random backoff to make sure that you do not collide with the other person sending on that wifi channel. If the other person keeps sending reset packets, that means you will not be able to transmit. That means your side of the connection can get held back.
With enough traffic you are able to pull out the same pieces of TCP data

In short:

+ The time it takes you to contact another computer on the network with be **longer** if that computer is "holding up" the network by sending acknowledgements to the site it is communicating with.
+ The time it takes you to contact another computer on the network with be **shorter** if that computer is NOT "holding up" the network by sending acknowledgements to the site it is communicating with.

**The attack**:

+ The authors show that it is possible to detect whether a spoofed packet is successfully acknowledged as authentic by a victims computer, just by using the shared state (the half duplex nature of 802.11).

#### Spectre

The paper: [Spectre Attacks: Exploiting Speculative Execution](https://spectreattack.com/spectre.pdf)

**Lesser known fact:**

CPUs perform "speculative execution" to increase processor speed (run faster). The idea of speculative execution has been around for several decades. Speculative execution is when the CPU "guesses" what branch control flow will follow. For instance, instead of waiting for a value from external memory the program will attempt to "save time" by continuing down a guessed path and return to this register state when the value is retrieved from memory to verify it took the correct path. If the path was correct - time was saved! If the path was incorrect - the process resumes at the saved register state and proceeds (this time taking the correct branch) consuming the same amount of time as if it had remained idle the entire time.

**The attack**:

+ (1) Introduce a sequence of instructions into the process address space that acts as a covert channel transmitter (leaks the victim's memory/register contents)
+ (2) Induce speculative execution to erroneously run the instruction sequence in (1)
+ (3) Victim's information is leaked over the covert channel in (1).

#### Meltdown

The paper: [Meltdown](https://meltdownattack.com/meltdown.pdf)

Meltdown is similar to Spectre but subtly different. Meltdown's exploit relies on: out of order execution, while for Spectre the exploit relies on: speculative execution (branch prediction). Meltdown accesses kernel memory from user space. [Kernel page-table isolation or, KPTI](https://en.wikipedia.org/wiki/Kernel_page-table_isolation) effectively mitigates Meltdown (but not Spectre).

More information: [Reading privileged memory with a side-channel](https://googleprojectzero.blogspot.com/2018/01/reading-privileged-memory-with-side.html)


## Thanks

+ Credit for the good stuff goes to [Zakir Durumeric](https://zakird.com/), newly minted security professor at Stanford, mistakes are mine!
+ You can get a survey of security topics by reading through the selected papers for the class Zakir is teaching, [CS 356 - Topics in Computer and Network Security](https://cs356.stanford.edu/)
+ Credit goes to [Feross Aboukhadijeh](https://feross.org/) for finding the visual microphone video
