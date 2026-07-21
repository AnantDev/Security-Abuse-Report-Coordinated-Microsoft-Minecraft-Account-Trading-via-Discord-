# Security-Abuse-Report-Coordinated-Microsoft-Minecraft-Account-Trading-via-Discord-

Executive Summary

This report documents an organized ecosystem operating primarily through Discord that distributes compromised Microsoft accounts associated with Minecraft and other Microsoft services.
During this investigation, numerous Discord communities were observed openly advertising and distributing Microsoft accounts, Minecraft accounts, redeemable codes, and account bundles through both free and paid channels.
Several of these communities have memberships ranging from hundreds to more than 10,000 users, with many additional communities operating in parallel.
The ecosystem appears highly organized, involving automated checking software, disposable email services, password-changing utilities, and structured resale operations.
The purpose of this report is to assist Microsoft's Security Response Center (MSRC) by documenting publicly observable infrastructure and providing evidence to support further investigation.
Investigation Overview
Over several weeks, multiple Discord communities involved in Microsoft account trading were observed and documented. Observed activities include:
	•	Distribution of Microsoft accounts
	•	Sale of Minecraft Java accounts
	•	Distribution of Minecraft redeem codes
	•	Automated account checking and bulk credential verification
	•	Password-changing tools used after accounts are obtained
	•	Disposable email abuse to facilitate account creation
	•	Automated account resale and marketplace activity
	•	Unverified account-generation claims
Scale of the Problem
Based on direct observation during this investigation:
	•	100+ Discord servers identified
	•	Several servers with 10,000+ members
	•	Hundreds of Microsoft/Minecraft accounts shared daily across servers
	•	Both free and paid/premium account marketplaces in operation
	•	Bots used to automate distribution and sales
Typical Workflow
Based on observed evidence, these communities appear to operate through a repeatable pipeline:
	•	Large collections of email/password combinations are acquired from unknown upstream sources.
	•	Automated tools test whether the credentials are still valid.
	•	Accounts linked to Minecraft or other Microsoft services are identified.
	•	Valuable accounts are categorized (e.g., by Minecraft skins, rare usernames, linked purchases).
	•	Accounts are distributed for free or sold through Discord servers.
	•	New credentials are continuously sourced and processed, keeping the pipeline active.
This report does not claim to establish how any individual credential set was originally obtained; that determination is left to Microsoft's investigation.
Evidence Collected
1. Discord Servers
Evidence includes documentation of servers distributing Minecraft accounts, Microsoft accounts, combo lists, premium "drops," and organized account marketplaces. A list of currently active servers observed to be involved in this activity is included in Appendix A.
2. Credential Evidence
A sample output log from a checking tool was reviewed, containing 131 lines recorded over an approximately eight-minute window on July 13, 2026. Each line paired a Microsoft account email address and password with a Minecraft gamertag, indicating the tool had automatically validated the credentials against Microsoft's login and Minecraft's linked-account service in real time. The email domains observed were predominantly hotmail.com, outlook.com, live.fr, and similar Microsoft-owned domains, consistent with mass-checking of previously leaked combo lists rather than targeted attacks.
Actual account credentials from this sample are withheld from this report. They are available separately, on request, through a secure and appropriate channel for Microsoft's investigators.
3. Automated Credential Checkers
Publicly shared automation capable of testing large numbers of credentials was identified during this investigation. Reviewed tooling exhibited the following characteristics:
	•	Multi-threaded credential testing
	•	Proxy support to distribute request origin
	•	Automated login requests against Microsoft services
	•	Automatic categorization of results (valid/invalid/high-value)
	•	Telegram-based notifications for successful hits
These characteristics indicate purpose-built software for large-scale, automated credential verification against Microsoft accounts. A copy of one such checker script was obtained during this investigation; its source code is withheld from this report and can be provided to Microsoft's security team directly on request.
4. Password-Changing Utilities
Tools advertised as Microsoft account password-changing utilities were found being promoted inside these Discord communities, apparently used to lock in control of an account once credentials are obtained. One such utility was obtained and reviewed as part of this investigation; its source code and executable are withheld from this report and are available to Microsoft's security team directly on request. Microsoft should assess whether these tools rely on legitimate recovery flows, abuse of active sessions, or previously compromised credentials.
5. Disposable Email Services
Several disposable/temporary email providers are commonly referenced within these communities, including Temp-Mail, Emailnator, YOPmail, Email Generator, and EmailMux. These services have legitimate general uses, but are frequently used within this ecosystem to automate account creation and reduce attribution:
	•	Temp-Mail — temp-mail.org
	•	Emailnator — emailnator.com
	•	YOPmail — yopmail.com
	•	Email Generator — emailgenerator.org
	•	EmailMux — emailmux.com
These are general-purpose public services, not abuse tools in themselves; they are listed here only because they recur frequently in the observed communities' workflow.
6. Public Repositories and Tooling
Publicly accessible repositories appearing to relate to Microsoft account checking or automation were identified. These should be reviewed by Microsoft's security team to determine whether they violate Microsoft's Terms of Service or facilitate credential abuse.
Impact
	•	Unauthorized access to Microsoft accounts
	•	Minecraft account theft and loss of purchased content
	•	Direct financial loss to affected users
	•	Increased support burden on Microsoft/Mojang
	•	Erosion of user trust in account security
	•	Marketplace fraud and repeated account resale
	•	Ongoing, automated credential abuse at scale
Recommendations
Improve Abuse Detection
	•	Increase detection of high-volume login attempts
	•	Flag automated/bot-like login behavior
	•	Detect and block known proxy abuse patterns
	•	Strengthen credential-stuffing defenses
Detect Checker Signatures
	•	Identify known automation patterns and tooling fingerprints
	•	Flag common request headers used by checker tools
	•	Monitor for repeated/patterned API usage consistent with checkers
Increase Platform Collaboration
	•	Coordinate with Discord Trust & Safety to remove servers dedicated to credential distribution and account marketplaces
	•	Share indicators of compromise across platforms where relevant
Repository Monitoring
	•	Monitor public code repositories distributing credential checkers or Microsoft account automation tools
	•	Pursue takedown requests where tooling clearly facilitates unauthorized access
Strengthen Account Protection
	•	Encourage broader MFA and passkey adoption
	•	Expand risk-based authentication and device verification
User Awareness
	•	Warn users against purchasing Minecraft or Microsoft accounts from third parties
	•	Discourage credential sharing
	•	Educate users on the risks of "free account" servers
Evidence Package Summary
The complete evidence package assembled during this investigation includes:
	•	Screenshots of Discord servers and marketplace activity
	•	Examples of automation/checker tooling
	•	Samples illustrating credential-list structure (without reproducing real account data)
	•	References to public repositories
	•	References to public websites used by these communities
	•	Archived Discord messages
Sensitive evidence (raw credential data, full tool source, or archived chat logs) is being withheld from this document and can be provided directly to MSRC through a secure channel upon request.
Request to Microsoft
I respectfully request that Microsoft's Security Response Center review this material to determine:
	•	Whether these communities violate Microsoft's policies
	•	Whether the identified tools facilitate unauthorized access to Microsoft accounts
	•	Whether additional protections can be implemented to reduce abuse affecting Microsoft customers
I am willing to provide additional evidence, timestamps, archived material, and further documentation on request, through an appropriate secure channel.
Reporter Contact Information
	•	Name: Anant
	•	Background: B.Tech student, AI/ML, India
	•	Location: Delhi, India
	•	Email: SoseYv9canant@gmail.com
	•	Discord username: raptor_ji
	•	Discord user ID: 1072733945667538985

Appendix A: Discord Servers Observed
This appendix is intended solely for MSRC / Discord Trust & Safety review as part of a takedown investigation. It should not be published, screenshotted, or shared publicly — doing so would circulate active invite links to the same abusive communities this report is trying to get shut down.
