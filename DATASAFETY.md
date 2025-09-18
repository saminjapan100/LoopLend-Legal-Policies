LoopLend Data Safety Documentation

Effective Date: September 18, 2025
Last Updated: September 18, 2025  

This Data Safety Documentation explains what user data LoopLend collects, how it’s used, and whether it’s shared with third parties, in compliance with Google Play Data Safety requirements. LoopLend is a hyper-local sharing platform that enables users to lend and borrow physical items (e.g., tools, gear, gadgets) within a 5-mile radius (or 10-mile for premium users) using a token-based system. We collect only the minimum data needed to provide a secure, trust-driven, and sustainable lending experience. We do not sell your personal data.
This document is publicly available on our GitHub repository at https://github.com/LoopLend/legal-policies. The version on our website (https://looplend.app/data-safety) and in-app is authoritative. Historical versions are available on GitHub for transparency.

1. Overview
LoopLend is committed to protecting your data and fostering trust in our community-driven platform. We use industry-standard security measures, including encryption in transit (HTTPS/TLS) and at rest (Firebase defaults), and restrict access to authenticated users via Firebase security rules. This document details the data we collect, its purpose, sharing practices, and your control options, ensuring transparency for our users.

2. Data Types Collected and Shared

The table below summarizes the data LoopLend collects, why we collect it, whether it’s shared, and how it’s protected. All data is encrypted in transit, and users can request deletion unless otherwise noted.


Data Category       |      Examples         |   Purpose of Collection   |     Is Data Shared with Third Parties?     |      Encrypted in Transit?     |     Can Users Request Deletion?


Personal Info           Email address,          Account creation, user         Yes — stored in Firebase (Google);                ✅ Yes                           ✅ Yes
                        display name,             profile display,               display name/photo visible to 
                     optional profile photo     communication between                 loop participants
                                                        users



Identity               Optional blurred        User verification for           Yes — stored securely in Firebase                 ✅ Yes                           ✅ Yes
                      government-issued ID     trust badges (e.g.,               Storage, not shared publicly
                                                 “Gold Looper”) 



Location            Precise GPS location (      Show nearby items,             Yes — processed by Google Maps SDK                ✅ Yes                           ✅ Yes (disable in device settings)
                     5-mile radius, or         suggest safe meeting           for matching; not stored permanently
                     10-mile for premium       spots (e.g., parks, 
                           users)                    cafes)


Financial Info       Token purchase data,       Enable token economy          Yes — processed securely by Google Play            ✅ Yes                           ✅ Yes
                     premium subscription      ($0.99/5-$4.99/50) and              Billing/Apple In-App Purchases
                       info ($2.99/mo)            premium features



User-Generated      Item listings (photos,       Power lending loops,        Yes — listings/messages visible to loop            ✅ Yes                           ✅ Yes
   Content          descriptions), messages,   facilitate communication,     participants; stored in Firebase Firestore
                      reviews, ratings               build trust



App Activity        Listings posted, tokens    Improve features, prevent     Yes — stored in Firebase Firestore/Analytics       ✅ Yes                           ✅ Yes (opt-out for analytics)
                       earned/spent, loop       fraud, track engagement 
                     completions, analytics     (anonymized analytics)
                         events (e.g., 
                       “loop_completed”, 
                        “token_bought”)




Device Info           Device model, OS, IP           Fraud detection,             Yes — processed by Firebase and                ✅ Yes                          ✅ Yes
                        address, device            security, analytics                react-native-device-info
                       fingerprint (via 
                     react-native-device-info)



Crash &             Crash logs, error reports      Diagnose and fix bugs,          Yes — via Firebase Crashlytics                ✅ Yes                          ✅ Yes
Performance                                        improve app stability
Data




In-App Messages       Chat content, push          Facilitate communication         Yes — stored in Firebase Firestore;           ✅ Yes                          ✅ Yes
& Notifications      notification tokens,        (e.g., “Loop started! Timer:     delivered via Firebase Cloud Messaging 
                        delivery data              2:00:00 ⏰🔄”), send                       (FCM)
                                                          updates 


Photos/Media             Item photos,               Verify transactions,            Yes — stored in Firebase Storage;            ✅ Yes                          ✅ Yes
                     pickup/return proof            enforce double-token              visible to loop participants
                                               deposits (hash difference >20%)

 



3. Third-Party SDKs and Libraries
LoopLend integrates trusted third-party SDKs and libraries to provide core functionality. Below is a list of SDKs that may process or transmit user data off the device, along with their purposes:

Firebase SDKs (Google):
Authentication: Email or anonymous OTP login.
Firestore: Stores user profiles, listings, messages, and transaction data.
Storage: Holds item photos and blurred IDs (<5MB, compressed).
Cloud Messaging (FCM): Delivers push notifications (e.g., loan updates, fraud alerts, weekly tips like “Strong loops = public meets!”).
Analytics: Tracks anonymous events (e.g., “loop_completed”, “token_bought”) to improve the app.
Crashlytics: Collects crash logs and performance data for debugging.


Google Maps SDK:
Provides map views, geolocation for 5-mile radius matching, and Safe Spot suggestions (e.g., parks, cafes).
May transmit IP address and location queries to Google.


Google Play Billing / Apple In-App Purchases:
Processes token purchases ($0.99/5-$4.99/50) and premium subscriptions ($2.99/mo).
LoopLend does not access or store payment card details.


AdMob SDK (Google):
Displays non-personalized banner ads for non-premium users.
Uses device IDs for ad delivery and performance tracking.


react-native-device-info:
Collects device identifiers for fraud prevention (e.g., detecting suspicious accounts).


expo-notifications:
Manages push notification tokens and delivery via FCM.


Insurance Providers (if applicable):
For optional coverage for high-value items, limited data (e.g., item details, user ID) may be shared with consent.


Future Partnerships:
“Sponsored Loops” (v2) may involve anonymized data sharing with partners, subject to user opt-in.



All SDKs follow industry-standard privacy and security practices. Refer to our Privacy Policy for links to third-party policies.


4. Data Transfer Between Servers and Apps

Server-to-Server:
LoopLend’s Firebase backend (project ID: looplend-d325b, hosted in the U.S.) communicates with Google servers for authentication, notifications, analytics, and payment validation.
No user data is shared with unapproved third parties.


On-Device Transfers:
Data is not automatically shared with other apps on your device unless you initiate sharing (e.g., sharing an item listing link via a messaging app).


WebView:
The app may use WebView to display the Privacy Policy, Terms of Service, or help documentation.
Anonymous click analytics (via Firebase Analytics) may track WebView interactions to improve usability. Users can opt out of analytics via in-app settings.




5. Data Security and Retention

Security Measures:
Firebase Security Rules: Firestore and Storage access is restricted to authenticated users (e.g., allow read, write: if request.auth != null;).
Encryption: All data is encrypted in transit (HTTPS/TLS) and at rest (Firebase defaults).
Photo Limits: Item photos and blurred IDs are compressed (<5MB) and stored securely in Firebase Storage.
Fraud Prevention: Device fingerprinting (via react-native-device-info), photo hash checks (>20% difference via Cloud Functions), and keyword/geo filters protect against suspicious activity.


Retention Periods:
Account/Profile Data: Retained until you request deletion via in-app settings or privacy@looplend.app.
Location Data: Cached for 24 hours in AsyncStorage for offline sync, then deleted.
Transaction Data: Kept for 7 years to comply with tax and financial regulations.
Messages/Listings: Retained for 1 year after a loop ends, unless deletion is requested.
Fraud Reports: Kept for 3 years for safety and legal purposes.
Analytics/Crash Data: Anonymized and retained indefinitely to improve the app, unless opted out.




6. User Rights and Controls
LoopLend provides robust controls to manage your data:

Access, Correction, Export, Deletion: Request access to, correction of, export of, or deletion of your data via in-app settings or by emailing privacy@looplend.app.
Opt-Out Options:
Notifications: Disable marketing or transactional push notifications (e.g., weekly tips) in-app or via device settings.
Location: Disable precise location access in device settings (limits nearby item matching).
Analytics: Opt out of Firebase Analytics via in-app Privacy Settings.
Ads: Opt out of AdMob ad personalization via device settings (e.g., Limit Ad Tracking on iOS, Opt Out of Ads Personalization on Android) or by emailing privacy@looplend.app for CCPA opt-out.


CCPA Rights (California Residents):
Request details about collected or shared personal information.
Request deletion, subject to legal exceptions (e.g., tax records).
Opt out of data sharing for ads (LoopLend does not sell data; see https://looplend.app/do-not-sell).


GDPR Rights (EEA Residents):
Restrict or object to data processing (e.g., analytics).
Withdraw consent for optional features (e.g., location, notifications).


Response Time: We respond to requests within 30 days (or 45 days for complex CCPA requests).


7. Children’s Data
LoopLend is not directed to children under 13 (or 16 in the EEA under GDPR). We do not knowingly collect data from minors and rely on users to self-report their age. If we discover data from a child, we will delete it promptly. Contact privacy@looplend.app if you believe we have collected such data.


8. Policy Updates
We may update this Data Safety Documentation to reflect new features, SDK changes, or regulatory requirements. Material changes will be communicated via in-app notifications (using Firebase Cloud Messaging), email, or an updated GitHub commit at https://github.com/LoopLend/legal-policies. The “Last Updated” date will reflect the latest version.


9. Contact Us
For questions or concerns about data safety, contact:
LoopLend Privacy Team📧 
privacy@looplend.app🌐 
https://looplend.app/data-safety  
For transparency, this document and its historical versions are available on our GitHub repository at https://github.com/loopland-legal-policies.


10. Summary for Users
To make this document easier to understand for our LoopLend community, here’s a quick summary:  

What We Collect: Email, optional ID/photos, temporary location (24hr cache), tokens, and app activity to power safe lending loops. 🔄  

How We Use It: To match you with nearby items, verify transactions, prevent fraud, and improve the app.  

Sharing: Only with trusted providers (e.g., Firebase, Google Maps) and loop participants (e.g., your profile photo). We don’t sell your data.  

Your Control: Delete your data, opt out of ads, analytics, or notifications, and disable location anytime.  

Security: Everything’s encrypted, with access limited to authenticated users.  

Questions? Email privacy@looplend.app—we’re here to keep your loops safe! ⏰
