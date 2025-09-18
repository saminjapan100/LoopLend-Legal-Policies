LoopLend Terms of Service

Effective Date: September 18, 2025
Last Updated: September 18, 2025  

Welcome to LoopLend (“LoopLend,” “we,” “our,” or “us”), a community-driven platform for lending and borrowing physical items (e.g., tools, gear, gadgets) within a local radius using a token-based system. These Terms of Service (“Terms”) govern your use of the LoopLend mobile application, website, and related services (collectively, the “Services”). By downloading, installing, creating an account, or using the Services, you agree to be bound by these Terms and our Privacy Policy. If you do not agree, please do not use our Services.
These Terms are publicly available on our GitHub repository at https://github.com/LoopLend-legal-policies. This version and the in-app version are authoritative. Historical versions are available on GitHub for transparency.


1. Purpose of LoopLend
LoopLend enables users to lend and borrow physical items within a hyper-local 5-mile radius (or 10-mile for premium users), fostering sustainability, reducing waste, and building trust through a gamified token system (no cash for core trades). Our mission is to create strong community loops where users share responsibly and safely. 🔄


2. Eligibility
To use LoopLend, you must:

Be at least 18 years old (or the age of legal majority in your jurisdiction).
Be legally capable of entering into a binding contract.
Reside in a country where LoopLend operates (currently available nationwide in the United States, with potential expansion to other regions).
Not be a person barred from using the Services under applicable laws.

Children’s Restrictions: LoopLend is not intended for users under 13 (or 16 in the European Economic Area under GDPR). We rely on users to self-report their age and do not knowingly allow use by children below these ages.
By using the Services, you represent and warrant that you meet these eligibility requirements.


3. Account Registration

Registration: You must create an account using a valid email address or anonymous one-time password (OTP) login via Firebase Authentication.
Account Security: You are responsible for maintaining the confidentiality of your login credentials and for all activities under your account.
Accurate Information: You agree to provide accurate, current, and complete information during registration and to update it as needed.
Account Responsibility: You are liable for any misuse of your account, including unauthorized access due to failure to secure your credentials.


4. Tokens, Deposits, and Payments
a. Token System
LoopLend uses in-app tokens for lending and borrowing transactions. Tokens:

Are earned by lending items or completing successful loops.
Can be purchased via Google Play Billing or Apple In-App Purchases ($0.99 for 5 tokens to $4.99 for 50 tokens).
Are subject to a 20% cap on purchased tokens to ensure fairness in the community.
Have no cash value, are non-transferable, and cannot be redeemed for money or other currencies.

b. Deposits

A double-token deposit is required for each loan to ensure trust and accountability.
Deposits are held in escrow via Firebase Cloud Functions until the item is returned, as verified by photo proof (pickup/return, hash difference >20%).
If an item is not returned within the agreed loan duration plus a 24-hour grace period, LoopLend may initiate mediation. Deposits may be forfeited to the lender or refunded based on mediation outcomes.

c. Fees

LoopLend charges a 5% service fee on token deposits to support platform operations.
A premium subscription ($2.99/month via Google Play Billing or Apple In-App Purchases) provides priority listings, a 10-mile radius, an ad-free experience, and a 50% token bonus on purchases.

d. Refunds

Token purchases and subscriptions are subject to the refund policies of Google Play or Apple App Store.
Deposits are refunded to the borrower upon verified item return. Non-return disputes are resolved via mediation (see Section 9).
LoopLend does not offer cash refunds for tokens or subscriptions, as tokens have no monetary value.

e. No Cash Transactions
LoopLend is not a marketplace for direct sales or cash-based rentals. All transactions must use the in-app token system.


5. User Responsibilities
As a LoopLend user, you agree to:

Accurately describe items you list (e.g., condition, functionality, loan duration, token cost).
Return borrowed items on time and in the condition received, accounting for normal wear and tear.
Meet in safe, public locations (e.g., parks, cafes suggested as “Safe Spots” by LoopLend).
Upload truthful photo proof of item handoff and return, as required by the platform.
Communicate respectfully and professionally with other users via in-app chat.
Comply with all applicable local, state, and federal laws during transactions.

You agree not to:

Post or exchange illegal, stolen, hazardous, or prohibited items (e.g., weapons, drugs).
Engage in fraudulent, deceptive, or scamming behavior (e.g., misrepresenting items, falsifying photo proof).
Use LoopLend for commercial rental businesses or sales without express written permission from LoopLend.
Circumvent security measures, manipulate ratings/tokens, or use automated scripts/bots to interact with the Services.
Harass, threaten, or defame other users or post inappropriate content.


6. Trust, Ratings, and Enforcement

Ratings: After each completed loop, users rate each other (1-5 loop-stars) based on reliability, communication, and item condition.
Trust Badges: Earn a “Gold Looper” badge by completing 5 successful trades and verifying your identity with a blurred government-issued ID.
Enforcement: Users with an average rating below 3 stars after 5 reports may be automatically suspended. LoopLend reserves the right to investigate disputes, suspend, or permanently ban accounts for:
Violating these Terms.
Engaging in fraud, theft, or abusive behavior.
Harming the community or platform integrity.


Appeals: Suspended users may contact legal@looplend.app to appeal, subject to LoopLend’s discretion.



7. User Content and Messaging

Content Ownership: You retain ownership of content you create (e.g., item listings, photos, messages) but grant LoopLend a worldwide, non-exclusive, royalty-free, transferable license to use, store, display, and process such content solely to operate, promote, and improve the Services.
Messaging: You may exchange messages via LoopLend’s real-time Firestore chat (e.g., auto-messages like “Loop started! Timer: 2:00:00 ⏰🔄”). Messages are subject to review for fraud/theft prevention or dispute resolution.
Prohibited Content: You agree not to post or send:
Harassing, abusive, threatening, or defamatory content.
Spam, unsolicited advertising, or scams.
Illegal, obscene, or inappropriate material.


Content Removal: LoopLend may remove or flag content that violates these Terms or applicable laws.



8. Fraud and Theft Prevention
To ensure a safe and trusted community, LoopLend implements:

ID Verification: Optional blurred government-issued ID for trust badges, stored securely in Firebase Storage.
Device Fingerprinting: Uses react-native-device-info to detect suspicious activity.
Photo Verification: Requires photo proof for item handoff/return, with Cloud Functions checking for >20% hash difference to confirm authenticity.
Double-Token Deposits: Ensures accountability for loans, with a 24-hour grace period.
One-Tap Reporting: Allows users to report fraud/theft via a lime green “Report Scam/Theft” button, logged to Firestore for investigation.

Accounts engaging in fraudulent, abusive, or illegal behavior may be suspended or banned, with no refund of tokens or subscriptions.


9. Dispute Resolution
LoopLend provides an in-app mediation process for disputes, including non-returned items or disagreements:

Both parties may upload photo proof to support their claims.
LoopLend reviews evidence (e.g., photos, chat logs, ratings) within 24 hours.
Outcomes may include releasing deposits to the lender, refunding the borrower, or escalating to further mediation.
LoopLend’s decision on in-app token disputes is final.

For disputes beyond tokens (e.g., legal claims), see Section 14 (Governing Law & Arbitration).


10. Intellectual Property

LoopLend’s IP: The LoopLend name, logo (infinity loop to handshake), designs, code, and content are owned by LoopLend and protected by copyright, trademark, and other intellectual property laws. You may not copy, modify, distribute, or reverse-engineer LoopLend materials without our written consent.
User Feedback: Any feedback, suggestions, or ideas you provide about the Services may be used by LoopLend without compensation or attribution, and you grant us a perpetual, royalty-free license to use such feedback.


11. Third-Party Services
LoopLend integrates with third-party services, including:

Firebase (Google): For authentication, database (Firestore), storage (photos, IDs), and push notifications (FCM).
Google Maps: For geolocation (5-mile radius, Safe Spots).
AdMob (Google): For non-personalized banner ads for non-premium users.
Google Play Billing / Apple In-App Purchases: For token and subscription payments.
Insurance Providers: For optional “$1/day coverage” for high-value items (if selected).

Use of these services is subject to their respective terms and privacy policies, linked in our Privacy Policy. LoopLend is not responsible for third-party service performance or policies.


12. Disclaimer of Warranties
LoopLend provides the Services “AS IS” and “AS AVAILABLE,” without warranties of any kind, express or implied, including but not limited to:

The accuracy, availability, or quality of item listings.
The condition, functionality, or safety of borrowed/lent items.
The conduct, reliability, or identity of other users.

You use LoopLend at your own risk. We recommend verifying users, meeting in public Safe Spots, and insuring high-value items. 🔄


13. Limitation of Liability
To the maximum extent permitted by law:

LoopLend is not liable for any loss, theft, damage, injury, or disputes arising from your use of the Services, including item exchanges or interactions with other users.
Our total liability will not exceed the greater of (a) $50 USD or (b) the amount you paid to LoopLend in the past 12 months (e.g., token purchases, subscriptions).
LoopLend is not responsible for indirect, incidental, special, consequential, or punitive damages, including loss of profits, data, or goodwill.



14. Indemnification
You agree to indemnify, defend, and hold harmless LoopLend, its affiliates, officers, directors, employees, and agents from any claims, liabilities, damages, or costs (including reasonable attorneys’ fees) arising from:

Your violation of these Terms.
Your misuse of the Services (e.g., posting illegal items, fraud).
Your violation of any third-party rights (e.g., intellectual property, privacy).
Disputes with other users during loops.



15. Governing Law and Arbitration

Governing Law: These Terms are governed by the laws of the State of Delaware, USA, without regard to conflict of law principles.
Arbitration: Any dispute arising from or relating to these Terms or the Services will be resolved through binding arbitration under the rules of the American Arbitration Association (AAA) in Delaware, on an individual basis. You waive any right to participate in class actions, class arbitrations, or jury trials, except where prohibited by law.
Exceptions: Claims for injunctive relief or intellectual property disputes may be brought in a Delaware court.
Costs: Each party will bear its own arbitration costs, unless otherwise determined by the arbitrator.


16. Termination

By LoopLend: We may suspend or terminate your account at our discretion if you:
Violate these Terms or other LoopLend policies.
Engage in fraud, theft, abuse, or illegal activity.
Harm the community or platform integrity (e.g., manipulating ratings).


By You: You may terminate your account at any time via in-app settings or by contacting legal@looplend.app.
Effect of Termination: Upon termination, you will lose access to your account, tokens, and loop history. No refunds will be provided for tokens or subscriptions.


17. Force Majeure
LoopLend is not liable for any failure or delay in providing the Services due to events beyond our reasonable control, including but not limited to natural disasters, pandemics, server outages, or third-party service disruptions (e.g., Firebase, Google Maps).


18. Changes to Terms
We may update these Terms periodically to reflect changes in our Services or legal requirements. Material changes will be communicated via in-app notifications (using Firebase Cloud Messaging), email, or an updated GitHub commit at https://github.com/LoopLend-legal-policies. Continued use of the Services after updates constitutes acceptance of the revised Terms.


19. Contact Us
For questions or concerns about these Terms, contact us at:
LoopLend Legal Team📧 
legal@looplend.app
  
For transparency, these Terms and their historical versions are available on our GitHub repository at https://github.com/LoopLend-legal-policies.


20. Summary for Users
To make these Terms easier to understand for our LoopLend community, here’s a quick summary:  

What LoopLend Is: A platform to lend and borrow items locally using tokens, not cash. 🔄  

Your Responsibilities: List items accurately, return them on time, meet in safe spots, and be respectful. Don’t post illegal stuff or scam anyone.  

Tokens & Fees: Buy tokens ($0.99-$4.99), pay double-token deposits, and a 5% fee. Premium ($2.99/mo) gives you perks like ad-free use.  

Safety: We use photo proof, ID verification, and fraud checks to keep loops safe. Report issues with one tap.  

Your Risk: Use LoopLend at your own risk—verify users and insure valuables. We’re not liable for damages.  

Questions? Email legal@looplend.app. 

Let’s keep the loops strong! ⏰
