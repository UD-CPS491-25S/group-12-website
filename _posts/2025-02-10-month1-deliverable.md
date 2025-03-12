---
layout: post
title: "Month 1 Sprint"
subtitle: "Initial architecture and planning of the Turtle Up app"
date: 2025-02-10 
background: "/img/posts/05.jpg"
---

## Table of Contents

1. [Technology Stack and Architecture](#i-technology-stack-and-architecture)
   - [Frontend](#frontend)
   - [Backend](#backend)
   - [Database](#database)
   - [Architecture Diagram](#architecture-diagram)
2. [Development Progress](#iii-development-progress)
   - [Current App Design](#current-app-design)
3. [Direction and Prospects](#iii-direction-and-prospects)
   - [Priorities](#priorities)
   - [Features](#features)
   - [Other Actions](#other-actions)

---

<br>

## I. Technology Stack and Architecture

---

#### Frontend:

- **Framework**: React Native
  - Framework for developing mobile applications (iOS and Android) on a single codebase
  - Bridges JavaScript (in our case TypeScript) code to platform-native components
- **Metaframework**: Expo
  - Framework built on top of React Native, a wrapper
  - Allows for prototyping and deployment without needing to set up native development environments like Xcode or Android Studio
  - **Expo Go**: Mobile app that allows for preview and testing in real time
- **Language**: TypeScript
  - JavaScript with static typing
- **Maps**: Google Maps API, react-native-maps
  - Maps APIs for displaying locations and paths

#### Backend:

- **Go**
  - Mainly used for handling POST requests to send data to Firebase
  - Decided for future-proofing, has extensive documentation, allows for implementation of AI features

#### Database:

- **Firebase**
  - Shared database with other Turtle Up group
  - Utilize Firebase SDK to handle GET requests to retrieve data
  - Decided for Firebase's efficient real-time updates to clients

#### Architecture Diagram:

![Architecture Diagram](\group-12-website-jekyll\img\posts\capstone-turtle-up-month-1-architecture.jpg)

---

<br>

## II. Development Progress

---

#### Current App Design:

- **Home**: General information on turtles the user has supported through purchasing the Turtle Up bracelets
- **Map**: Turtle locations and paths
- **Shop**: Purchase items and donate to Turtle Up
- **About**: Resources about Turtle Up

![Current App Design](\group-12-website-jekyll\img\posts\capstone-turtle-up-month-1.jpg)

---

<br>

## III. Direction and Prospects

---

#### Priorities

- Finalize basic functionality of the app
- Implement sign-up, authentication, and database functionality
- Integrate Turtle Up resources (podcasts, donations, links, etc.)

#### Features:

- **End of Month 2 Features**:
  - SSO: Users can create an account or link with an available external account (Google, iCloud, etc.)
  - Shop Page: Handling secure transactions
  - Map Integration: Ability to display static data on the map page.
- **Future Features**:
  - Biometric authentication
  - AI implementation
  - Webview integration of Turtle Up Education game

#### Other Actions:

- Daily SCRUM meetings with both groups, regularly updating progress
- Team hackathon activity, possibly with other Turtle Up groups

<br>
