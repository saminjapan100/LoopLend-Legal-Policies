LoopLend Privacy Policy

Effective Date: September 18, 2025
Last Updated: September 18, 2025  

LoopLend (“we,” “our,” or “us”) is a mobile app and platform designed to foster a hyper-local sharing economy, enabling users to lend and borrow physical items (e.g., tools, gear, gadgets) within their communities. We are committed to protecting your privacy and building trust through transparency. This Privacy Policy explains how we collect, use, store, protect, and share your information when you use the LoopLend mobile app, website, and related services (collectively, the “Services”). By using LoopLend, you agree to this Privacy Policy.  
This policy is publicly available on our GitHub repository at https://github.com/LoopLend/legal-policies. The version on our website (https://looplend.app/privacy) and in-app is authoritative. Historical versions are available on GitHub for transparency.

1. Our Commitment to Privacy
LoopLend’s mission is to create a sustainable, trust-driven platform for local item sharing, reducing waste and building community connections. We do not sell your personal information. Your data is used solely to provide, improve, and secure our Services, prevent fraud, and comply with legal obligations. Our “No data selling” commitment is core to our community-driven ethos, ensuring safe and fun lending loops for all users.

2. Information We Collect
We collect the following categories of information to operate LoopLend effectively and provide a seamless experience:
a. Account and Profile Data

Mandatory: Email address (or anonymous one-time password login via Firebase Auth), display name.
Optional: Profile photo, government-issued ID (blurred for trust badge verification, stored securely in Firebase Storage).
Generated: Loop history (items lent/borrowed, ratings, reviews, number of loops), token wallet balance, premium subscription status (e.g., $2.99/mo for ad-free experience, priority listings).

b. Device and Technical Data

Device type, operating system, app version, IP address, unique device identifier (via react-native-device-info for fraud prevention).
Crash logs and performance metrics (via Firebase Analytics, anonymized).
Usage data (e.g., app interactions, page views) to improve functionality and accessibility.

c. Location Data

Precise Location: Used only to show items within a 5-mile radius and suggest safe exchange locations (e.g., parks, cafes) via expo-location and Google Maps.
Temporary Use: Location data is cached for 24 hours in AsyncStorage and not stored permanently.
Opt-In: Location access requires your explicit consent and can be disabled in device settings or in-app.

d. Transaction Data

Token purchases, deposits (double-token for loans), refunds, and premium subscription details (processed via Google Play Billing or Apple In-App Purchases).
Loan timers, photo proofs for item pickups/returns (stored in Firebase Storage, compressed to <5MB).
Fraud/theft reports and related metadata (e.g., report timestamps, user IDs).

e. User-Generated Content

Item listings (photos, names, descriptions, loan durations, token costs) created via Formik modals.
Messages exchanged with other users via real-time Firestore chat (e.g., auto-messages like “Loop started! Timer: 2:00:00 ⏰🔄”).
Ratings (1-5 loop-stars), reviews, and fraud/theft reports submitted via the app.

f. Notifications and Analytics

Push notification preferences and delivery data (via Firebase Cloud Messaging, e.g., loan updates, fraud alerts, weekly safety tips like “Strong loops = public meets!”).
Anonymous analytics events (e.g., “loop_completed”, “token_bought”, “fraud_report”) to improve Services and track engagement.


3. How We Use Your Information
We use your information to deliver a secure, fun, and community-driven experience, specifically to:

Facilitate lending and borrowing of items, including matching users within a 5-mile radius and suggesting safe exchange spots.
Process token purchases ($0.99/5-$4.99/50), double-token deposits (with 5% app fee), and refunds via Google Play Billing or Apple In-App Purchases.
Verify identities and prevent fraud/theft (e.g., blurred ID checks, photo hash comparison with >20% difference via Cloud Functions, device fingerprinting).
Send push notifications for loan updates, fraud alerts, and weekly safety tips.
Display non-personalized banner ads to non-premium users via AdMob.
Analyze usage to enhance app performance, accessibility (e.g., VoiceOver support), and user experience.
Comply with legal obligations, such as tax reporting or responding to law enforcement requests.


4. Legal Bases for Processing
We process personal data under the following legal bases, as applicable:

Contractual Necessity: To provide the Services you request (e.g., creating an account, posting listings, completing loops).
Legitimate Interests: To ensure trust and safety (e.g., fraud prevention, device fingerprinting), improve app functionality, and send transactional notifications.
Consent: For optional features like precise location access, marketing emails, or push notifications.
Legal Obligation: To comply with laws (e.g., tax regulations, responding to legal requests).

For users in the European Economic Area (EEA), these bases align with GDPR requirements. For California residents, see Section 9 for CCPA-specific rights.


5. Data Sharing and Disclosure
We do not sell your personal information. We may share limited data with the following entities under strict conditions:
a. Service Providers

Firebase (Google): For authentication (email/anonymous OTP), database (Firestore for users, items, messages), file storage (photos, blurred IDs), push notifications (FCM), and anonymized analytics.
Google Maps: For geolocation services (5-mile radius matching, safe spot suggestions using Maps SDK for Android and Geocoding API).
Google Play Billing / Apple In-App Purchases: For processing token purchases ($0.99/5-$4.99/50) and premium subscriptions ($2.99/mo).
AdMob (Google): For serving non-personalized banner ads to non-premium users (uses device ID for ad delivery).

b. Other Users

Limited profile data (display name, profile photo, loop history, ratings, trust badges like “Gold Looper”) is visible to users you interact with during a loop to foster trust.

c. Legal and Safety Purposes

We may disclose data to comply with legal obligations (e.g., tax authorities), respond to law enforcement requests, or protect the rights, property, or safety of LoopLend, its users, or the public.

d. Business Transfers

In the event of a merger, acquisition, or sale of assets, your data may be transferred to a successor entity under strict confidentiality agreements.

e. Insurance and Partnerships

If you opt for “$1/day coverage” for high-value items, limited data (e.g., item details, user ID) may be shared with insurance partners, with your consent.
Future “Sponsored Loops” (v2) may involve sharing anonymized data with partners, subject to your explicit opt-in consent.


6. Data Storage and Security

Storage Location: Data is stored on Firebase servers hosted in the United States (project ID: looplend-d325b).
Security Measures:
Firestore and Storage access is restricted to authenticated users (auth-only rules, e.g., allow read, write: if request.auth != null; for Firestore).
Data is encrypted in transit (HTTPS/TLS) and at rest (Firebase defaults).
Blurred IDs and photo proofs are compressed (<5MB) and stored securely in Firebase Storage.
Fraud prevention includes device fingerprinting (react-native-device-info), photo hash checks (>20% difference via Cloud Functions), and keyword/geo filters for listings.


Retention Periods:
Account/Profile Data: Retained until you request deletion via in-app settings or privacy@looplend.app.
Location Data: Cached for 24 hours in AsyncStorage, then deleted.
Transaction Data: Kept for 7 years to comply with tax and financial regulations.
Messages/Listings: Retained for 1 year after a loop ends, unless deletion is requested.
Fraud Reports: Kept for 3 years for safety and legal purposes.




7. Cookies and Tracking Technologies
LoopLend does not use traditional cookies but employs similar technologies, such as:

Device Identifiers: For authentication sessions and fraud prevention (via react-native-device-info).
Analytics: Firebase Analytics tracks anonymous events (e.g., “loop_completed”, “token_bought”) to improve Services. You can opt out via in-app settings.
Ads: AdMob uses device IDs to serve non-personalized ads to non-premium users. You can opt out via device settings (e.g., Limit Ad Tracking on iOS, Opt Out of Ads Personalization on Android).


8. Ads and Monetization

Banner Ads: Non-premium users see non-personalized AdMob banner ads at the bottom of listing screens (test ID: ca-app-pub-3940256099942544/6300978111). Ads do not use personally identifiable data.
Token Purchases and Subscriptions: Processed securely via Google Play Billing ($0.99/5-$4.99/50 tokens) or Apple In-App Purchases ($2.99/mo premium for priority listings, 10-mile radius, ad-free experience, +50% token boost).
Future Partnerships: “Sponsored Loops” (v2) may include promotional content, with clear opt-in consent.


9. Your Privacy Rights
Depending on your jurisdiction, you have the following rights:
a. General Rights

Access: View the personal data we hold about you.
Correction: Update inaccurate or incomplete data.
Deletion: Request deletion of your account and data.
Portability: Export your data (e.g., loop history, profile) in a machine-readable format.
Opt-Out: Disable marketing emails, push notifications, or location services via in-app settings.

b. CCPA Rights (California Residents)

Right to Know: Request details about the categories and specific pieces of personal information we collect, use, or share (e.g., account, location, transaction data).
Right to Delete: Request deletion of your personal information, subject to legal exceptions (e.g., tax records).
Right to Opt-Out of Sale: LoopLend does not sell personal information, but you can opt out of ad-related data sharing (e.g., AdMob device ID usage) via device settings or by emailing privacy@looplend.app. Visit https://looplend.app/do-not-sell for details.
Non-Discrimination: We will not discriminate against you for exercising your CCPA rights.

c. GDPR Rights (EEA Residents)

Restriction: Limit how we process your data in certain cases (e.g., during dispute resolution).
Objection: Object to processing based on legitimate interests (e.g., analytics).
Withdraw Consent: Revoke consent for optional features (e.g., location, notifications) at any time.

To exercise your rights, contact us at privacy@looplend.app or use the “Privacy Settings” in the app. We will respond within 30 days (or 45 days for complex requests under CCPA).


10. Children’s Privacy
LoopLend is not intended for children under 13 (or the age of digital consent in your country, e.g., 16 in some EEA countries). We do not knowingly collect data from children and rely on users to self-report their age. If we discover data from a child, we will delete it promptly. Contact us at privacy@looplend.app if you believe we have collected such data.


11. International Data Transfers
LoopLend is hosted in the United States (Firebase servers, project ID: looplend-d325b). By using the Services, you consent to the transfer, storage, and processing of your data in the U.S., which may have different privacy laws than your country. We implement safeguards (e.g., encryption, Firebase security rules) to protect your data in compliance with GDPR and other regulations.


12. Changes to This Policy
We may update this Privacy Policy to reflect changes in our Services or legal requirements. Material changes will be communicated via in-app notifications (via expo-notifications), email, or an updated GitHub commit at https://github.com/LoopLend/legal-policies. The “Last Updated” date will reflect the latest version.


13. Contact Us
For questions, concerns, or to exercise your privacy rights, contact us at:
LoopLend Privacy Team📧 
privacy@looplend.app🌐 
https://looplend.app/privacy  

For transparency, this policy and its historical versions are available on our GitHub repository at https://github.com/LoopLend/legal-policies.


14. Summary for Users
To make this policy easier to understand for our LoopLend community, here’s a quick summary:  

We Don’t Sell Your Data: Your information is used only to power lending loops, prevent fraud, and improve the app.  

What We Collect: Email, optional ID/photos, temporary location (24hr cache), and transaction details to make loops safe and fun.  

Your Control: Opt out of ads, notifications, or location sharing anytime. Request data deletion or export via in-app settings or privacy@looplend.app.  

Security: Your data is encrypted, with access restricted to authenticated users. Blurred IDs and photo proofs are securely stored.  

Questions? Email us at privacy@looplend.app—we’re here to help! 🔄
