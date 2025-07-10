---
title: "Technical aspects"
description: "At this stage, your business requirements are clear. Now, let's address the associated technical requirements."
summary: "At this stage, your business requirements are clear. Now, let's address the associated technical requirements."
tags: ["business analysis"]
date: "2025-07-10"
draft: false
series: ["Software Business Analysis"]
series_order: 4
showEdit: false
---
At this stage, your **business requirements are clear** (refer to the previous article [Documenting Your Needs Effectively]({{< ref "posts/202507-2-Documenting-your-business-need.md" >}})). Now, let's address the associated **technical requirements**.
As mentioned in the prerequisites, no IT knowledge is required. In this article, you'll become familiar with the main technical concepts, which you can then integrate into your specifications. This will significantly increase your project's chances of success because, as with business aspects, your service provider won't be forced to implicitly make incorrect choices since everything will already be detailed in your specifications.

## Every detail is important (Again)
Don't just skim over the technical aspects. **Dig deep into them from the start in your specifications**, because any subsequent changes will incur costs, or even lead the project to a dead end.
So, mention every detail you've gathered, ask questions to your IT department, and get clarification on the most obscure points from ChatGPT. You don't need to become an expert yourself, just to have a comprehensive overview of your technical expectations.

## Application type
You must start by choosing the **type(s) of application**:
* **Desktop application** (specify if Windows and/or macOS)
* **Website**
* **Web application** (specify if desktop / tablet / smartphone)
* **Mobile application** (specify if Android and/or iOS)
* **Script**

Sometimes, multiple types are possible. For example, a restaurant chain will need a website for visibility and Google search ranking, and a mobile application for customers to place orders.
Note that a development technique called "**responsive design**" allows a website or web application to be used on a computer, tablet, and smartphone by slightly changing its appearance based on screen size. However, this technique doesn't cover all use cases of a true mobile application, which is sometimes the best choice.

## Integration
It's highly likely that your application will need to **interact with your existing enterprise ecosystem**: your ERP, CRM, invoicing software, etc.
Another possibility is that you've selected a provider to process your payments, like Stripe.
In both cases, it's imperative to **mention it clearly in your specifications**. Don't forget to specify the relevant version (e.g., Sage X3) and its hosting mode (e.g., Deployed on Amazon Cloud), as these are important technical details.
This point is often treated too lightly, often towards the end of a project, even though it's a strong constraint on your application. If your new e-commerce site ultimately doesn't connect to your order management ERP because your version isn't supported, your new website is unusable “as is”.

## Data Import and migration
Unless you're a newly formed company, it's likely your new application will need to be **initialized with your existing data**. For example, deploying a new CRM will involve loading your current Excel spreadsheet that lists your 500 customer and prospect contacts.
Therefore, mention in your specification that such an **import of a 500-line Excel file must be possible**.

## Data export
This point is more related to your application's end-of-life, in a few years, but it should be anticipated if you choose an existing market application.
To be able to import data from an old application into its replacement (refer to the previous point), the old application must also have an **export function in a "neutral" format**, readable by the new application as standard.
To date, the most robust and universal export implementations are **text file exports, CSV files, and SQL scripts**.

## Volume to be processed and number of users
In your specification, provide an **order of magnitude for the number of users and the volume of data to be handled**. Indeed, not all applications are designed to work with similar volumes. Amazon doesn't have the same volume requirements as a student selling scented candles online, although both are e-commerce businesses.
Furthermore, many SaaS solutions bill their service per user, and even desktop applications must adhere to the "1 user, 1 license" rule. Therefore, it's important to know this number before starting the selection process.

## Operation and support
**Operation and support are crucial for your application's longevity**. An SLA (Service Level Agreement) defines the expected performance and availability levels from your provider, clarifying their support commitments.
You can define requirements for response times and bug fixes, depending on the severity of the anomaly. The basic idea is to **agree in writing before such an incident occurs, not during it**!

## Application security
In your new application, **IT security must be a non-negotiable requirement**. Your reputation with your customers, as well as the risks of financial losses or disclosure of your company's strategic data, depend on it.

It will be difficult for me to cover all aspects of this rather technical subject in a single article, but I'll still give you some important ideas:
* Even for an internal company application, adopt a **Zero Trust approach**, where no user or device is considered trustworthy by default, even if it's on your corporate network.
* All digital exchanges must therefore be **secured**, using HTTPS for example, even within your corporate network.
* Create a requirement for **user authentication** (verification of their identity).
* Create another requirement for **authorization management** (to determine what each user is allowed to do in the application). This mechanism should only give the user access to the functions and data they need to work, never more.
* For "sensitive" functions (typically application administration actions like adding or modifying accounts), create an **audit requirement** so that the application records these types of sensitive actions separately.
* The type of data handled by the application can directly influence the security requirements your application must meet, for example, patient health data, payment information, or users' personal information.
* If you plan to have a custom application developed, I recommend also engaging a **third party to perform a security audit of the application's source code** with each new version, to ensure everything is as secure as possible and identify potential vulnerabilities. Your application's developer will then need to correct any reported anomalies before you accept delivery.
* If you're considering subscribing to a SaaS solution, it will be crucial to **verify with its provider that it meets your security requirements**, as you're entirely (and blindly) delegating the security of your data to them.
* Finally, a **robust backup strategy** is essential to protect your data against any unforeseen loss. A program can be replaced, but data cannot…

## GDPR and cookie compliance
**GDPR compliance** and **cookie management** are essential legal obligations for any application that processes the personal data of European users. This includes obtaining explicit consent for the use of cookies (you've already seen these on sites you use personally).

Keep in mind that regulations can vary by country or even region, and sometimes the constraint is set not by the physical location of your server or company, but by **where your users are located**. For GDPR, as with other regulations, non-compliance can lead to significant penalties, so it's crucial to integrate it from the design phase.

## Audience measurement
**Audience measurement** allows you to understand how users interact with your application and who they are (country, age group, access type, etc.). This information is truly important for **evaluating your application's performance, identifying its weaknesses (even some bugs), and guiding future improvements based on real-world data, not assumptions**.

For example, you might have launched an application initially in French. Now, does your audience measurement confirm that's sufficient? You might be surprised to see how many of your visitors are foreign and only stay on your site for a short time because they don't understand the language.

One of the most well-known tools is **Google Analytics**, which allows you to track visits, user behavior, and conversions for e-commerce sites. You can then create custom dashboards in tools like **Power BI or Excel** to "play" with the raw data, extract business insights, or visualize this data in charts. 

## Prioritization of technical requirements
As with the business requirements discussed in the previous article "<2 - Documenting Your Needs Effectively>", **extract and summarize the technical requirements from your specification document** to complete the same Excel spreadsheet, this time with one row per technical requirement. 

Then, categorize each of these rows according to its importance:
* **Mandatory**: This requirement is essential for the application to be selected (if purchasing an existing application) or must be developed (if it's a custom application).
* **Important**: This requirement will be a decisive criterion in the selection process or must be developed as a priority.
* **Optional**: This requirement will be a secondary criterion in the selection process, or its development can be done if there's budget remaining after the implementation of all "Mandatory" and "Important" requirements.

## Contact
Feedback is always welcome! Feel free to contact me by email [contact(at)candle8.app](mailto:contact@candle8.app) or on LinkedIn.
