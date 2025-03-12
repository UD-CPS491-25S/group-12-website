---
layout: post
title: "Month 2 Sprint"
subtitle: "Accomplishments, challenges, and planned improvements"
date: 2025-03-10
background: "/img/posts/06.jpg"
---

## Month 2 Reflection
Over the last month, we have made significant progress in pursuit of our goal to deliver an MVP to Dr. Corrine Brion and Turtle Up that is more than just the barebones product. Just as we hoped to, we hit the ground running this sprint and saw immediate progress through the implementations of user authentication, map interactivity, embedding of company resources, and creating a one-stop shop for the user seeking to contribute to Turtle Up.

Specifically, we made substantial progress towards a uniform OS experience singing in with Google SSO, created a modern map interface that updates in real time thanks to cloud functions, leveraged RSS feeds to present the user with all blogs, articles, and podcast episodes that are hosted by Turtle Up, and presented the user with the opportunity to both donate and view hypothetical bracelets for purchase without having to leave the application.

All of these feature implementations allowed us to take ownership of our part of the app in a unique way, giving our work some individuality from the other TuT development team while still fostering a healthy working and collaborative relationship with the other TuT team.

Moving into Month 2, we felt very confident in our technology stack’s ability to assist us with some of our key features. Though it has been helpful, there have been a number of instances of emergent features or behaviors in our application due to unanticipated cooperation between different levels of the tech stack or differences in OS.

To address the first point, we believed working with Firebase would be almost seamless, and at first it very much was. For basic login, Firebase was flawless as the SDK had many functions that handled exactly what we were seeking to address. The moment we took a step towards SSO integration with Google was where the difficulties began to arise.

After some painstaking work with a React Native library that promised to clean up the communication between mobile platforms and the Google Cloud, we had to backtrack and use embedded redirects within the mobile application that still allowed us to leverage Firebase’s functions which unfortunately has proven to be ineffective on Android platforms but it is working on Web and iOS (C. Moody, I. Motlagh).

To the second point, React Native was our solution to building an app that could be supported regardless of platform due to its ability to integrate native elements which relieved us of the responsibility of having to tailor an application to that specific OS. Overall, it has accomplished this, but our configuration leveraging Expo has proven to be slightly problematic.

As we progressed through the map interactivity function listed above, we made the decision to create a uniform element that would include more detail than the native map elements (particularly iOS). This would leverage Google Maps API and present a user with a Google Maps display regardless of their OS. Unfortunately, Expo did not support this, but fortunately we were able to side step with the React Native Maps Expo plugin which delivered the presentation we hoped for (Z. Rice).

Another example of some interesting behavior from React Native is within our shop page, where we have a carousel highlighting products (bracelets) that are for sale. For some reason, this element does not get along with the Gesture Handler very well, which is essential for mobile interactivity via the touchscreen.

The conflict was leading to page stack elements flashing whenever a user navigated from the shop page putting the carousel in the background. We are still actively working on a permanent solution for this, but in the meantime are un-rendering the carousel when it’s out of focus. However, this introduces some delay for the carousel to be re-rendered when returning to the shop page (M. Nguyen, Z. Rice).

Despite all the frustrations of these technological roadblocks, we are confident and eager to keep on pressing on towards our final product. Though frustrating, these features were essential for us to overcome as we seek to deliver an application that is dynamic (carousel, map interactivity), modern (SSO), and satisfactory to Turtle Up for their goals to allow a user to view real-time Turtle Data and make monetary transactions in order to support Turtle Up.

Briefly wanted to mention collaboration over the last month with the other TuT development team, it has been going great. Through all of the uncertainties of customer direction, both teams have maintained a commitment to communicating progress, questions, and direction.

Having the two teams has given each the ability to go deeper into the application which will certainly make the finished proof of concept feature rich.



## Month 3 Plan
Looking ahead to the next month, the foundation has been set for us to build out and introduce some nuance and sophistication to our key features.

Currently, the progress we have made is good, but it could be so much better with more time, which is what the next month will allow us to do. As we move closer to the proof of concept we are delivering, these are the following features we hope to incorporate into our application over the next month of developments:

- Trajectory Visualization: As the cron job runs via the Google Cloud Scheduler functionality and pings data to turtle objects, rather than showing the current position we aim to show the current point and the previous X number of points (X to be determined). Users should also have the ability to see specific turtle trajectories, likely via a dropdown selection or checkbox. 
- Security Improvements: Overall, we have been trusting of the functions we are leveraging to maintain security which is bad practice. We seek to harden our application, especially our Go Backend, via secure data transmission, appropriate data transmission, and secure storing of credentials to protect the sensitive information housed in our application. 
- Stripe Paid Transactions: Hope to present Turtle Up with a working prototype representing Stripe’s ability to handle the transactions to purchase bracelets within the application. Going to ask Dr. Brion in our presentation Thursday March 11, 2025 about their current payment system and how we can integrate into it.

These are the notable programmatic features we are striving to accomplish in Month 3, and we believe that these features move the Turtle Up Tracking Application one step closer to production level.

Beyond programming, we are also going to prioritize documentation over the next month. Thorough documentation ensures a smooth transition if this project were to ever be picked up by a future capstone group or another outside development group, which is of deep importance to us.

Knowing that this is a proof of concept leaves room for improvement and also shifting in direction if Turtle Up chooses to move forward with some of our ideas and modify others. We want to make that as easy as possible for them and the next group of developers, and we will maintain close communication with our client in order to do so.
