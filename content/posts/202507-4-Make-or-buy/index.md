---
title: "Make or Buy?"
description: "You can now determine whether the best option for you is to choose an existing 'off-the-shelf' solution, or to select a service provider who will develop your application 'custom-made'."
summary: "You can now determine whether the best option for you is to choose an existing 'off-the-shelf' solution, or to select a service provider who will develop your application 'custom-made'."
tags: ["business analysis"]
date: "2025-07-10"
draft: false
series: ["Software Business Analysis"]
series_order: 5
showEdit: false
---

Thanks to the previous articles [Documenting Your Needs Effectively]({{< ref "posts/202507-2-Documenting-your-business-need.md" >}}) and [Technical Aspects]({{< ref "posts/202507-3-Technical-aspects.md" >}}), you've produced a consistent and exhaustive Word document listing all your business and technical needs, as well as an Excel workbook containing the same summarized and prioritized list of requirements.
Armed with these two documents, you can now determine whether the best option for you is to choose an existing "off-the-shelf" solution, or to select a service provider who will develop your application "custom-made".

## Buy
Choosing to **buy an "off-the-shelf" solution** means selecting existing software platforms that meet the needs outlined in your specification document.

You'll encounter different economic models from application vendors:
* **Open source**: Often free, but sometimes with a paid variant offering vendor support and/or extended features.
* **Annual or monthly subscriptions**: At a consistent price.
* **Initial purchase**: Followed by regular renewals, typically annually and at a lower price.
* **Lifetime purchase**: But keep in mind you'll likely need to pay later for future updates and continued vendor support.

Here's my approach for starting the search for a commercial application:
1. **For an overview**, I begin with an AI Chatbot (ChatGPT, Gemini, Copilot, etc.) with a general question like: "What are the best CRMs for small businesses with Amazon and Google Shopping integration?"
2. Once I have this "starting point," I visit **application catalogue sites** like Capterra or G2, beginning with the applications returned by the Chatbot. Then, I navigate within the same catalogue category to explore its competitors.
3. When I've narrowed down to **5 or 6 applications** that likely fit my needs, I visit each vendor's website for details, to read their documentation, etc. Your specification document and Excel workbook will provide the "checklist" to validate or rule out each application.
4. Finally, I conclude with a **search engine** (Google, Bing, etc.) to get external reviews on the 2 or 3 "finalist" applications from my selection: user reviews, forum discussions about the application, possibly books on Amazon, or if the application appears on job search sites.

There's a slightly particular case for buying **extensions for existing software**, sometimes available via the vendor's dedicated marketplace. If you already have their base application deployed in your company, you might find extensions that specifically meet your needs at a very reasonable cost compared to custom development. In this scenario, Browse the marketplace catalogue replaces steps (1) and (2)

## Make 
From my professional experience, I urge you to **carefully weigh the pros and cons of a custom-developed application**.
Certainly, it's the most flexible solution to check all the boxes in your Excel requirements workbook, as it will be developed precisely to meet those. However, be mindful of the **total cost and complexity**, throughout the entire application lifecycle, from conception to end-of-life.

A standard application, while less expensive, will be **easier to adopt** (due to existing documentation, training resources and trainers, internet forums, etc.). You'll have **minimal maintenance** because it will be handled by the vendor. However, you'll often have to adapt to its functionalities, as customization possibilities can quickly become limited.

A simple rule might be to choose custom development if you find yourself in one of these two cases:
* You want to **build your entire business around this single application**; it will be your product, or at least your primary production tool over which you must maintain control.
* At least one of your business or technical requirements classified as "mandatory" is **not offered in any commercial solution**.

In all other cases, **simplify your life and opt for an existing solution**, even if it means slightly adjusting your workflow and training your employees a bit longer on the new tool.
If you ultimately choose **custom development**, the first step is to find and select the right vendor. 

They should have at minimum a visible portfolio of successful applications and clients you can contact. Regarding domain knowledge, your expectations for your vendor will depend on your own level of domain expertise and the complexity of your application, keeping in mind that the more specialized a vendor is in a particular domain, the higher their daily rate tends to be.

Once you've identified a vendor, provide them with your **detailed specification document**, which will serve as the basis for their proposal. You are free to also share the Excel workbook, as it will inform them of your interest level for each requirement, and their pricing can take that into account.

Always request a **detailed breakdown of costs per part for each functionality**. This will allow you to understand the cost distribution and adjust, if necessary, especially for non-mandatory requirements. Don't hesitate to remove a requirement if its implementation cost outweighs the benefit you'll gain from it.

Finally, be clear with them from the outset on crucial aspects like **final ownership of the source code, bug fix timelines, and post-delivery support**.

## What about doing it yourself?
If you have the time and a certain aptitude for IT, there are some very good solutions for certain small projects with a limited scope, often for internal company use:
* **Microsoft 365 collaborative tools**: Shared Excel, Forms, etc.
* **Python scripts**: To replace an Excel macro or automatically extract data from a website, for example.

## Wrong good ideas
Next, here's what I consider to be "false good ideas" to avoid, in increasing order:
* **No-code platforms**: These are quite useful for quickly creating a simple prototype, but a drawback of their simplicity is that they quickly hit unavoidable technical limits. Moreover, you'll become literally "captive" to that platform, meaning you'd have to start everything from scratch if you wanted to change later.
* **Developing yourself with ChatGPT or Copilot**: Unless you've been a developer yourself, you'll tear your hair out trying to debug or evolve source code you don't understand, or worse, leave major security flaws in your application. Even for a simple webpage, the result might seem satisfactory at first on a desktop PC, until you discover its absolutely hideous appearance on a smartphone (try visiting https://olivier-essner-81.github.io/BeanScene/ on your smartphone).
* **Using an AI programming agent**: If you quickly browse YouTube, you'll find two camps: non-developers who claim to have successfully used them to create an application in 2 hours that earns them thousands of dollars per week (I'm barely exaggerating), and developers with serious backgrounds who have actually used them and can precisely detail the strengths and weaknesses of these tools. Joking aside, for now, these solutions aren't mature enough for my taste to be used by non-developers beyond a quick internal prototype. To date, I've never seen such agents design an internet-facing application that can evolve and be used for several years, taking into consideration security, scalability, future new needs, technical maintenance, GDPR, and so on.
* **Using a "pirated" version**: The worst idea...
  * **Legally**: Some software vendors have mandated third-party organizations to audit and verify software license compliance in companies (number, context of use, etc.). In cases of non-compliance, they will strongly urge you to conclude a regularization agreement with the vendor (needless to say, this will be non-negotiable and very favourable to the vendor!) to avoid criminal prosecution.
  * **Morally**: Some software vendors, especially smaller ones, literally stake their survival on selling their applications. A pirated version is a theft of their product, equivalent to your customers breaking into your factory at night to steal the machine tools you assemble, while you have no insurance against this type of loss.
  * **Extreme security risk**: Some hackers modify and freely distribute a "pirated" version of an application. You download and install it – great, it works! Except that, in addition to the application, a malicious program has silently self-installed (a true story from the inside [schneider-electric-data-breach-microminder-cyber-security](https://www.linkedin.com/pulse/schneider-electric-data-breach-microminder-cyber-security-ex2dc/). This program might, for example, wait for you to log into your banking website, then use your session to perform transactions on your behalf, from your computer, while authenticated to your own account... In short, it's the best way to transfer your entire company bank balance to Moldova!

## Contact
Feedback is always welcome! Feel free to contact me by email [contact(at)candle8.app](mailto:contact@candle8.app) or on LinkedIn.
