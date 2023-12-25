---
layout: post
title: Activity4
subtitle: Smart Phones Security
categories: Activities
tags: [activities, smart phones, security]
---

## Smart Phones Security

Today's smartphones hold all the keys to our communications, finances, data, and social lives, which makes these ubiquitous devices lucrative targets for cybercriminals. There are billions of smartphone users worldwide, and none can completely avoid cyberattacks. Spam, phishing, malicious apps, and ransomware are only some of the threats that mobile device users face today and the attack techniques get more sophisticated every year. To stay protected, we need to understand and recognize the most common threats to smartphone security. This is our guide to what those threats are, the best defenses for avoiding those threats, and what to do if you suspect your device has been compromised. 

# What is the Android attack surface?

The Android operating system and the mobile devices it runs on dominate the market in comparison to other device manufacturers. Along with the market share, the Android ecosystem is heavily fragmented; that is to say, many individuals are still using older versions of the Android operating system. This makes it a prime target for hackers as older versions of Android have less hardened security measures in place. One of the main goals of an attacker when dealing with the local attack surface is to elevate his/her privileges to achieve code execution as the root or system users. Sockets can be used by non-privileged applications to communicate with higher-privileged applications. Android often uses sockets as a form of Inter-Process Communication (IPC). IPC allows applications and services to communicate with each other and synchronize their data and actions. Many applications in the Android Operating System expose different forms of IPC to non-privileged applications making up part of its local attack surface. In addition to sockets, Android also uses shared memory and its Binder driver to implement IPC mechanisms. Android implements its form of shared memory via a mechanism called Anonymous Shared Memory (ashmem). The Binder driver facilitates communication with Android applications via Intents. All of these IPC mechanisms can be leveraged to possibly attack higher privileged processes from an unprivileged context since communication between contexts is possible. The goals of the attacker remain pretty much the same when dealing with the remote attack surface, but here the attacker may just be content with getting code execution remotely and then pivoting to the local attack surface to exploit a privilege escalation vulnerability. Android shares some of the same remote attack surfaces as PCs. Technologies such as web browsers can be targeted remotely and have a large attack surface on their own, as they often must deal with executing application logic, rendering images, and other underlying protocols. What makes the remote attack surface different on a mobile device are technologies such as Bluetooth, Near Field Communication (NFC), and Baseband. While these technologies do allow for remote communications, they are more limited in range as compared to a technology that communicates over the Internet. The technology with the longest range is Baseband. The baseband is what facilitates cellular communications for the mobile device. Attackers can set up a Rouge Base Station to send malicious traffic to anything that connects to it. This works because the Baseband system-on-chip (SoC) will connect to the closest cell tower, or the tower with the strongest signal. The technology with the next longest range is Bluetooth. The range depends on the version of Bluetooth being used. Bluetooth 2.1 has a range of up to 100 meters as newer protocols such as Bluetooth 5.0 Low Energy can transmit and receive data up to 1000 meters away. VerSprite has previously published research that uses Bluetooth Low Energy to exploit an aftermarket remote start for an automobile. This exploit relied on reverse engineering the Android application to reveal the logic needed to perform the attack. The last of the technologies that represent the remote attack surface is Near Field Communication (NFC). NFC is often used for contactless payment and its range is usually less than 1 foot. The NFC protocol often uses the NFC Data Exchange Format (NDEF) whose messages can any type of data including URLs and images. The parsing of this data can lead to other applications being launched often with no user interaction.
![smart phone security](https://github.com/20802777/20802777.github.io/assets/148220693/e72a4ddb-cdcd-47b6-ad33-cd01cb3921fb)
Now we identify where the attack occurs based on this photo.


Android stack has its layers.
![android stack](https://github.com/20802777/20802777.github.io/assets/148220693/36508dfa-cc3e-4365-8ab7-00cd8b589bca)
This picture shows components running on the phone.

## References

9 top mobile security threats and how you can avoid them (no date) ZDNET. Available at: https://www.zdnet.com/article/9-top-mobile-security-threats-and-how-you-can-avoid-them/ (Accessed: 8 December 2023). 
Bigdrop (2023) Android attack surface: Hacking Android, VerSprite. Available at: https://versprite.com/blog/android-attack-surface/ (Accessed: 8 December 2023). 
