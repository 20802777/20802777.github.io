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

Security is a crucial aspect of the Android stack, and the platform incorporates various features and mechanisms to ensure the protection of user data, privacy, and the overall integrity of the system. Here are key security considerations at different levels of the Android stack:

1. **Linux Kernel Security:**
   - The Linux kernel forms the core of the Android operating system. It provides a robust security model with features such as user-based permissions, process isolation, and file system security.
   - SELinux (Security-Enhanced Linux) is used to enforce mandatory access controls, limiting the actions that system processes and apps can perform.

2. **Hardware Abstraction Layer (HAL):**
   - The HAL abstracts hardware-specific functionalities. Security at this level involves ensuring that hardware components are accessed securely and that communication between the hardware and the rest of the system is protected.

3. **Native Libraries and Android Runtime Security:**
   - Android Runtime (ART) employs various security mechanisms, including bytecode verification, to ensure the integrity of applications running on the platform.
   - Native code execution is subject to security best practices to prevent vulnerabilities like buffer overflows.

4. **Android Framework Security:**
   - The Android framework includes security features at the application layer. Key elements include:
      - **Permissions Model:** Android apps must declare the permissions they require, and users grant these permissions during installation.
      - **Application Sandboxing:** Each app runs in its own sandboxed environment, limiting its access to the system and other apps.
      - **Secure IPC (Inter-Process Communication):** Mechanisms like Intent-based communication are designed with security in mind.

5. **Application Layer Security:**
   - Android applications should adhere to secure coding practices to minimize vulnerabilities. Developers are encouraged to follow security guidelines provided by Android.
   - Code signing is used to verify the authenticity of apps, and the Android system enforces signature verification to ensure the integrity of the app during installation.

6. **Security Updates:**
   - Regular security updates are provided by Google to address known vulnerabilities and enhance the overall security of the Android platform. Device manufacturers and carriers play a role in delivering these updates to end-users.

7. **Secure Boot and Verified Boot:**
   - Secure boot processes ensure that only signed and authorized code is executed during the device boot-up sequence. Verified Boot checks the integrity of the system and warns users if the device has been compromised.

8. **Encryption:**
   - Android supports data encryption to protect user data. Full-disk encryption (FDE) and file-based encryption (FBE) are implemented to safeguard information in case of device loss or theft.

9. **Google Play Protect:**
   - Google Play Protect is a built-in security feature that continuously scans apps on the device and in the Play Store for potential threats. It helps identify and remove malicious apps.

10. **Network Security:**
    - Android supports secure network communication through protocols like HTTPS. Developers are encouraged to use secure communication practices, and Android provides APIs for implementing secure networking.

11. **Biometric Authentication:**
    - Android devices often incorporate biometric authentication methods like fingerprint recognition and facial recognition, adding an extra layer of security for device access.

In addition to these built-in security features, user education, safe app installation practices, and regular software updates are crucial aspects of maintaining a secure Android environment. Both users and developers play integral roles in the overall security of the Android ecosystem.

## References

9 top mobile security threats and how you can avoid them (no date) ZDNET. Available at: https://www.zdnet.com/article/9-top-mobile-security-threats-and-how-you-can-avoid-them/ (Accessed: 8 December 2023). 
Bigdrop (2023) Android attack surface: Hacking Android, VerSprite. Available at: https://versprite.com/blog/android-attack-surface/ (Accessed: 8 December 2023). 
