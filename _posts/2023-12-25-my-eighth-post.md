---
layout: post
title: Activity9
subtitle: My Experience With IoT
categories: Discussions
tags: [discussions, IoT]
---

## Have you used/experienced IoT devices in your daily life? How and what kind of projects did you build?

I think all of you know Siri or some of you use it daily. Siri is the virtual assistant Apple Inc. developed and integrated into various Apple devices, including iPhones. Siri is designed to respond to voice commands and perform tasks such as sending messages, making phone calls, setting reminders, providing information, and more. For my Python course, we had to make an assistant like Siri. To fulfill this assignment, first I started with a simplified code snippet that demonstrates the implementation of a few features, such as greeting the user, answering general knowledge questions, and providing weather information. Then I created a basic user interface using the Tkinter library in Python. I created a basic window using tk.Tk(). Inside the window, I added an entry widget (tk.Entry()) to allow the user to input their question. I also created a button (tk.Button()) with the label "Ask" and linked it to the handle_button_click() function using the command parameter.
When the user clicks the button, the handle_button_click() function is called. This function retrieves the user's question from the entry widget, calls the answer_question() function to get the answer, and displays the answer using a message box (messagebox.showinfo()).
To add voice recognition and speech synthesis capabilities to my AI assistant using Python, I used libraries such as SpeechRecognition for voice recognition and pyttsx3 for speech synthesis.
I used the SpeechRecognition library to recognize speech input from the user. I initialized the recognizer using sr.Recognizer() and use recognize_google() to convert the recorded audio into text.
For speech synthesis, I utilized the pyttsx3 library. I initialized the speech synthesizer using pyttsx3.init() and used the say() and runAndWait() functions to convert the response text into speech and play it.

Apple's HomeKit is a framework that allows smart home devices to work together seamlessly. You can use Siri to control HomeKit-compatible devices, such as smart lights, thermostats, locks, and more. Users can give voice commands to Siri to turn on lights, adjust the thermostat, or lock doors.

So I was thinking how fine it would be to grow my code and make something like Siri but with more capabilities. For example, You can select a language and talk to Siri in that language. But if you speak another language Siri gets confused and doesn't get the right voice commands. I want my device to recognize the language and respond in the same language or translate the voices in the moment. This way you don't need to choose your language and then command the assistant.

Also, not only the house, I want my device to be connected to my office computer so I can tell the AI assistant to write what I say in Word or do what I want with the application that I choose (e.g. Go to Cisco and create the network I'm going to define for you.). 

And lastly, Siri doesn't communicate with any particular hospital or doctor unless you put their number in the emergency call list. I want my assistant to get my medical history by searching for my name in big data or tracking my PC so when I tell it that I don't feel good it can call the hospital and get an appointment for me. 

Here is my code:

![Screenshot 2023-12-25 192654](https://github.com/20802777/20802777.github.io/assets/148220693/e9f1fd95-cd85-4943-b593-9f6360ae3208)
![Screenshot 2023-12-25 192721](https://github.com/20802777/20802777.github.io/assets/148220693/26fb46c5-3d1f-44e0-b631-bd9ae6f815cf)
![Screenshot 2023-12-25 192745](https://github.com/20802777/20802777.github.io/assets/148220693/b52a2186-2cd7-4a45-8882-07035e870b0b)
![Screenshot 2023-12-25 192811](https://github.com/20802777/20802777.github.io/assets/148220693/bea18cce-29df-4642-ab63-2cb3953cd024)
![Screenshot 2023-12-25 192834](https://github.com/20802777/20802777.github.io/assets/148220693/31c9474c-a1d1-4f6f-81e9-fc31ae04dc8b)

