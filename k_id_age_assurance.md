---
layout: page
title: "k-ID and the storage of sensitive information"
authors: "cheeseburger1337"
date: 2026-01-12
---
*I have done my best to provide accurate information in the article, however certain policies and regulations may change as time goes on. Archived versions of the websites I've accessed have been provided alongside the original links.*

In line with regulation changes in countries like the UK and Australia, Discord has implemented a new age verification process on their platform. They refer to this as "age assurance", and in [their article detailing the process](https://support.discord.com/hc/en-us/articles/30326565624343-How-to-Complete-Age-Assurance-on-Discord) ([alt](https://archive.is/MyM18)) they reveal it is delegated to a Singaporean company named "k-ID".

They also state that personal identity documents are deleted directly after age confirmation, and that facial age estimation data never leaves your device:
> Discord and k-ID do not permanently store personal identity documents or your video selfies. Images of your identity documents and ID match selfies are **deleted directly after your age group is confirmed**, and the video selfie used for facial age estimation **never leaves your device**.

Other companies using k-ID make similar statements, for example [Tumblr](https://help.tumblr.com/knowledge-base/verifying-your-age/) ([alt](https://archive.is/hxn1F)):
> Please note that neither Tumblr nor k-ID retain any media (e.g. ID documents) you provide for verification. This information is **deleted by the third-party age assurance provider once your age group is confirmed**. In addition, the video selfie used for facial age estimation **never leaves your device**, and Tumblr and k-ID only receive the outcome of that process.

We can also look at [Snapchat's statements](https://help.snapchat.com/hc/en-us/articles/43354851383828-Account-Restrictions-for-Australia-Users) ([alt](https://archive.is/5LnPG)):
> Photo ID: You can scan your government-issued photo identification and k-ID will validate your ID document and age. Your ID scan is only used to verify your age, and is **deleted once the process is complete**. Please note birth certificates are not supported.
> Facial Scan: You can take a selfie and k-ID will estimate an age range. Facial scan data is only processed locally and **never leaves your device**.

Looking at the [k-ID privacy policy](https://www.k-id.com/privacy-policy) ([alt](https://archive.is/zGATg)), this appears to be true. In Section 2A, k-ID states:
> Note, you only need to verify your age using one of the methods offered for your jurisdiction. **Regardless of what method you choose, k-ID does not receive the information you provide to prove your age status.** We only receive the results of the process.

But if k-ID doesn't recieve the information, then who does?

In Section 5A, k-ID reveals that they may share your personal information with certain "service providers" for age assurance:
> We may **share your personal information** with our third-party service providers and vendors that assist us with the provision of our Services. This includes service providers and vendors that provide us with IT support, hosting, identity verification, **age assurance**, payment processing, customer service, and related services. A list of k-ID’s subprocessors can be found at https://security.k-id.com/subprocessors.

Looking at k-ID's [list of "subprocessors"](https://security.k-id.com/subprocessors) (also found in Section 11C of their privacy policy), we can find
- **Stripe**, an American company listed as an "identity verification provider";
- **Veratad**, an American company listed as an "identity verification provider";
- **Privately**, a Swiss company listed as an "age estimation provider";
- **VerifyMy**, a British company listed as an "age estimation provider"; and
- **ConnectID**, an Australian company listed as an "age assurance provider".

Let's look at these companies a little further.

## Stripe

In [an FAQ page about their Stripe Identity service](https://support.stripe.com/questions/stripe-identity-faq) ([alt](https://archive.is/CxgMe)), under the heading "Consent to use your information", the article states that:

> Stripe retains biometrics for **one year** to identify fraud over time and across photo IDs, but you can opt-out at any time by contacting privacy@stripe.com. With this retained data, we also cross check new selfies against past submissions. As for the non-biometric data that you submitted (e.g., **photo and ID document**), Stripe retains that data in the business’ Stripe Dashboard for **3 years** and provides the business with the ability to delete it sooner.

This goes against the social media companies's previous claims of immediate deletion.

Stripe can also use customer's images to train their systems:

> Stripe **will use the captured images** to **improve the accuracy** of our biometric verification technology. This will help us reduce cases where we falsely reject legitimate users or approve fraudsters pretending to be someone else. If you give us permission, we will occasionally generate additional biometric identifiers for training purposes—which will be deleted **within one year**. You can withdraw your consent to Stripe’s use of your biometric information at any point by contacting us at privacy@stripe.com.

However, it appears this is optional:

> If you are not comfortable letting us use your data to improve our services, **you can click to decline consent** and we will only use your biometric information for the initial verification. You can learn more about how we handle and store your images and extracted data in our Privacy Policy.

## Veratad

In [Veratad's privacy policy](https://veratad.com/privacy-policy) ([alt](https://archive.is/h2ZEC)) under the heading "What information does Veratad collect, and how is it used and shared?", it is stated that:

> Pursuant to the contractual requirements with our clients and through the Client Services, we may collect information about individual end users including public and non-public records, **images of government-issued IDs, selfies**, and other personal information.

As for the retaining of this data, Veratad states:

> We and our third-party service providers and data partners **may retain and use this data** for legitimate interests (including retention of images for the improvement of our/their technology or as part of our Client Services), public interest and/or substantial public interest especially for crime/fraud prevention.

However, they do provide exceptions for certain regulations:

> (3) For **Illinois residents**, we will permanently destroy their biometric identifiers and biometric information when the initial purpose for collecting or obtaining such identifiers or information has been satisfied or **within 3 years** of the individual’s last interaction with Veratad’s Clients, whichever occurs first.
> (4) For **Texas residents**, we will permanently destroy their biometric identifiers the later of (1) **one year after the purpose for collecting the identifier expires**, or (2) **one year after any recordkeeping obligations imposed by law** in connection with the collection of the biometric identifier expires.
> (5) For **Washington residents**, we will retain their biometric identifiers **as long as reasonably necessary** to provide the service for which the biometric identifier was enrolled, and will permanently destroy their biometric identifiers thereafter.
> (6) For **Quebec residents**, we will permanently destroy their biometric identifiers **once the purposes for which personal information was collected or used are achieved**.
> (7) For **all other residents**, we will permanently destroy their biometric identifiers **once the purposes for which collecting or maintaining such information has been satisfied**.

This also goes against the social media companies's previous claims of immediate deletion.

## Privately

In [Privately's privacy policy](https://www.privately.eu/privacy-policy-en) ([alt](https://archive.is/wip/6lfem)) under the heading "What data does Privately Collect? How is it collected and what is it used for?", it is stated that for their "FaceAssure SDK":

> We **do not collect any user data** since end user relationships are managed by Clients themselves within their closed environments.

This seems to match Discord and k-ID's previous statements about facial recognition data being only stored on the end-user's device.

As for the use of user data in training their systems:

> We **do not use our customer’s data for training**. We train our machines separately on data specifically acquired for this purpose. We use data from a range of open, licensed sources or from manifestly public sources. Here we will collect both anonymous content to train our text model or photographs or videos of people and voices. We do not have any data information on any person that is not either licensed to us or is manifestly public. We may license such data or collect it from public sources.

## VerifyMy

In [VerifyMy's age assurance privacy policy](https://verifymy.io/age-verification-and-estimation/age-assurance-privacy-policy/) ([alt](https://archive.is/jW7cv)) under Section 6, It is stated that "images of your government-issued identification (including the image of you), and other pertinent information on that identification such as name, expiry date, document number" are stored for **28 days**. However, they provide exceptions for this figure:

> 1. where we provide age verification for adult sites in **certain jurisdictions** where we are prohibited by the laws of those jurisdictions from retaining identifiable personal information and therefore this data is deleted immediately after we have completed the age verification process; and 
> 2. where you do not successfully complete our age verification process, and **we believe you are a minor**, we will delete any personal data we hold immediately upon confirmation of such a result.

This still goes against the social media companies's previous claims of immediate deletion.

## ConnectID

In [ConnectID's privacy policy](https://connectid.com.au/privacy-policy/) ([alt](https://archive.is/ITXaV)), it is stated under Section 1 that:

> ConnectID facilitates third party **“Data Providers”** (such as banks, utility providers or government entities) to share identity information with **“Relying Parties”**s (such as e-commerce retailers or other service providers) where the relevant individual has consented to that sharing of identity information.
> Importantly, this transfer occurs directly between the relevant Data Provider and Relying Party, and **we do not access nor handle the shared identity information**. Further, each Data Provider and Relying Party are required under the rules that govern their participation in ConnectID to have their own privacy policy that applies to their participation in ConnectID.

Given that ConnectID's statements are true, it would be important to check with your chosen "Data Provider" and "Relying Party" in terms of the usage of your data.

## Summary

Despite the claim's of social media companies, images of your identity documents and ID match selfies are not necessarily deleted directly after your age group is confirmed. The use and retaining of user's identity documents and biometric data is determined by the service provider used by Discord's delegate, k-ID. While some providers may only process data locally on the end-user's device, others can keep user data for years and to train their systems. It is important to check your age verification method and the laws of your local jurisdiction to maintain control over your own personal information.

As stated by k-ID in Section 7 of their Privacy Policy:
> We do not accept liability for unauthorized access, use, disclosure, or loss of personal information.
