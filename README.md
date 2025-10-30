💬 InTouch — Real-Time Chat Application

InTouch is a modern, secure, and real-time chat application built with Android (Kotlin + Jetpack Compose) and Spring Boot (Kotlin) on the backend.
It enables users to connect instantly through private and group chats, share media, and receive notifications — powered by Firebase and MongoDB.

🚀 Features
👤 User Authentication

Secure sign-up & login using email and password

JWT-based authentication with encrypted passwords (BCrypt)

User profiles with name, bio, and profile picture support

💬 Real-Time Messaging

One-to-one chat using Firebase Realtime Database

Message status indicators: sent, delivered, seen

Auto-sync message backups in MongoDB

👥 Group Chat

Create and manage chat groups

Real-time message delivery for all group members

Group metadata stored in MongoDB

📸 Media Sharing

Send images, voice messages, and documents

Uploads handled via Firebase Storage

File URLs securely stored in MongoDB

🔔 Notifications

Push notifications using Firebase Cloud Messaging (FCM)

Instant alerts for new messages and group activity

🕒 Chat History & Sync

Persistent chat history stored in MongoDB

Retrieve past messages anytime via backend APIs

🏗️ Tech Stack
Frontend (Android)

Kotlin

Jetpack Compose

MVVM Architecture

Retrofit (for backend APIs)

Firebase Realtime Database & Storage

Firebase Cloud Messaging (Notifications)

Backend

Spring Boot (Kotlin)

MongoDB

JWT (Authentication)

Firebase Admin SDK

REST APIs for user and chat management

🧩 System Architecture
┌─────────────────┐    REST API + WebSocket    ┌──────────────────┐
│   Android App   │ ←────────────────────────→ │  Spring Boot     │
│   (Kotlin)      │                            │  Backend         │
│                 │                            │  (Kotlin)        │
│ • Jetpack Compose│ ←────────────────────────→ │ • JWT Auth       │
│ • MVVM          │    Firebase Real-time      │ • MongoDB        │
│ • Retrofit      │                            │ • WebSocket      │
│ • FCM           │                            │ • Firebase Admin │
└─────────────────┘                            └─────────┬────────┘
         │                                                │
         │ Firebase                                       │ MongoDB
         │ Real-time                                      │ Database
         ↓                                                ↓
┌──────────────────┐                            ┌──────────────────┐
│   Firebase       │                            │   MongoDB        │
│   Services       │                            │   Collections    │
│                  │                            │                  │
│ • Firestore      │ ←────Sync────→ │ • users     │
│ • FCM            │                │ • chats     │
│ • Storage        │                │ • messages  │
│ • Auth           │                │ • groups    │
└──────────────────┘                            └──────────────────┘

