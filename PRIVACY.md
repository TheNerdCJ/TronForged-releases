# TronForged Privacy Policy

Effective [EFFECTIVE DATE]. Published by Nycz Software Solutions with TronForged release 0.456.0. Each version of this policy is published with its release on the Release Feed and describes the Software as built at its effective date.

## 1. Who we are

Nycz Software Solutions, of [STREET ADDRESS], Hermiston, Oregon 97838, United States ("we", "us", the "Licensor"), is the author of TronForged (the "Software"). Contact: [CONTACT EMAIL].

The Software is licensed under the TronForged End User License Agreement (the "Agreement"; EULA.md, installed beside every console and published on the Release Feed). Words this policy capitalises - Shop, Customer, Authorised person, Technician, Shop server, Console, Release Feed, Third-Party Components - mean what they mean there. Where this policy and the Agreement differ about what the Software does, the Agreement governs.

## 2. The short version

We collect nothing about you through the Software. There is no TronForged cloud, account, relay or hosted service. Each repair shop (the "Shop") runs its own server on its own hardware, with its own keys, and the Software keeps the information it handles on that server and on the Shop's own computers and drives - never with us. The Software sends no telemetry, crash reports or customer data to us, and we cannot access, monitor, update, disable or connect to any Shop's server or any computer the Software runs on (Agreement, Section 3.2).

If you are a Shop's customer, your information is held by your Shop, not by us. Questions and requests about it go to your Shop (Section 9 below).

The only personal information we receive is what someone chooses to send us directly, for example by writing to [CONTACT EMAIL] (Section 8 below).

## 3. What this policy covers

This policy covers the Software: the installer, the three consoles (the Server Console, the Technician console and the Customer console), the Shop server program, the SYSTEM helper service, the remote agent service and the repair engine, and the releases we publish on the Release Feed (the public GitHub repository TheNerdCJ/TronForged-releases).

It does not cover how a Shop uses the information on its server; the Shop's own privacy notice does that. It does not cover GitHub, the tool vendors the Software downloads from, or the online services a Shop chooses to switch on; each of those has its own privacy terms. If a business connected with us also uses TronForged as a Shop, it does so as a Shop like any other: its customers' information is on its own server, under its own notice, and this policy does not cover it.

## 4. What the Software sends, and where

### 4.1 To the Shop's server

Every console is enrolled with one Shop server and talks to it over an encrypted connection. What the Software records about a Shop's staff, its Customers, the people a Customer names on its account and the computers the Shop services is kept on that server, not sent to us: account and contact details, tickets and messages, invoices and payments, backups, sign-ins, the audit log, remote-session records and the reporting described in Section 12 of the Agreement. A connected Customer console also lets the Shop see and control that computer, including while nobody is at it; sessions are logged, not recorded (Agreement, Sections 10 and 18).

That reporting includes a regular status beat from each enrolled console (such as the machine's name, Windows version, uptime, load and alert state) and diagnostic records about the Software's own behaviour (such as which repair steps failed and why, crashes and failed updates, and how a transfer of data between two computers ended). Paths, share names, email addresses, network addresses, host names, user names and card-number-shaped digits are removed or masked before diagnostic records leave the computer. These records go only to the Shop's server, which keeps them for the periods the Agreement states (Section 12.2). Nothing goes to us unless the Shop decides to send it to us.

The Software also keeps files on the computer it runs on - the connection details for the Shop's server, logs, reports and downloaded tools - in a data folder beside the program; Section 19.3 of the Agreement says who can open it. Backups, disk images and transfer packages that the Shop chooses to write to its own drives or network shares stay there (Agreement, Sections 13.1 and 13.5). None of this is sent to us.

### 4.2 To GitHub, when checking for releases

We publish releases on GitHub. Two parts of the Software read that public Release Feed:

- The installer, before it installs, reads the Release Feed once, anonymously, to see whether a newer installer exists, and downloads it if so. The check can be skipped. It sends nothing beyond an ordinary web (HTTPS) request. Installed consoles never contact the Release Feed (Agreement, Section 6.1).
- The Shop server checks the Release Feed about every six hours unless the Shop pauses its update pipeline, anonymously unless the Shop has stored its own GitHub token (Agreement, Sections 6.3 and 16.4).

Like any web request, these show GitHub the network (IP) address they come from and the time. GitHub's own privacy statement applies to them. We do not receive GitHub's records of who made a request. GitHub makes aggregate figures, such as how many times each release file has been downloaded, visible to the repository's owner; these do not identify anyone.

### 4.3 To vendors, when downloading tools and components

To repair a computer, the Software downloads tools and packages from their own vendors at run time - for example Microsoft, the PowerShell Gallery, the Windows Package Manager (winget) sources, computer makers' update utilities, the PawnIO project and the other tool vendors in Schedule A of the Agreement - and the Shop server may download Microsoft's and PawnIO's installers to serve to the Shop's consoles (Agreement, Sections 5.2, 5.3 and 11.4). These are ordinary download requests made on the Shop's behalf, never ours; each vendor sees the requesting network address under its own terms. The Software sends them nothing about the Shop's Customers.

### 4.4 To online services the Shop switches on

The Software can connect to the services below, only when the Shop configures them, under the Shop's own accounts and contracts. We are not party to any of them and receive nothing from them. Except where stated, all of this traffic leaves from the Shop server, never from a console.

- Square (Block, Inc.), for payments, invoices, saved cards, plans, catalog and stock: the items Section 16.1A of the Agreement lists, such as amounts, invoice lines and, for an invoice or a saved card, the Customer's name, company, email address and telephone number. A card is entered only on Square's own hardware or hosted pages, so the card details go to Square directly; the Software keeps only a card's brand, last four digits and expiry.
- Anthropic, for the optional AI features, off by default and switched on feature by feature (Agreement, Section 15). Depending on the features the Shop turns on, this can include the text of a support ticket, including what a Customer wrote on it. Consoles never call an AI provider.
- Address lookup, off by default (Agreement, Section 16.5): the address text a person at the Shop types, and nothing else about the Customer, to komoot's Photon service (OpenStreetMap data) or another Photon server the Shop names, and to the United States Census Bureau geocoder or another geocoder the Shop names.
- Sales-tax sources, off by default (Agreement, Section 16.8): the Streamlined Sales Tax Governing Board's rate and boundary files and the TaxLocus dataset are downloaded and receive nothing about Customers; the Census Bureau geocoder's geographies service and the Washington Department of Revenue's rate lookup receive the street address, city, state and ZIP code of the place a sale is taxed, and nothing else about the Customer.
- The Shop's own email provider (SMTP): invoices, sign-in details, ticket updates, appointment reminders, signed forms and the other emails Section 16.3 of the Agreement lists go out through the Shop's own mailbox. A console sends no email. Messages carry no tracking.
- Cloudflare, for the Shop's dynamic DNS if the Shop sets it up, and to learn the Shop server's own public address when the Shop advertises one.
- S3-compatible storage the Shop names, for off-site copies of backups, which the Shop server encrypts before they are stored (Agreement, Section 13.1).
- Amazon Business, for purchase orders the Shop approves: items, quantities and the Shop's delivery details, never Customer details.
- A web address the Shop names for notices of finished repair runs.

## 5. The Shop is in charge of its data; we are not

Where privacy law applies to the personal information on a Shop's server, the Shop is the controller (or "business", or the equivalent under the law that applies). We are neither a controller nor a processor of that information, and not a "service provider" or "contractor" for it: we do not receive it, store it, see it or have any means of reaching it, and the Software gives us no list of Shops or of their Customers (Agreement, Sections 3.2 and 9.4).

Because we have no access, we cannot answer for how a Shop collects, uses, shares, secures, keeps or deletes information, or notify anyone of a breach on a Shop's server; those duties are the Shop's (Agreement, Section 3.3). The Agreement requires each Shop to hold the authority and consent the law requires before it connects to a computer, and to tell its Customers what the Software does (Agreement, Section 9).
## 6. Children

The Software is a tool for repair businesses and is not directed to children. We collect nothing about anyone through it, children included. If a Shop holds information about a child - for example because it repairs a family computer - the Shop is responsible for any law that applies to that. If you believe a child has sent us personal information directly, write to [CONTACT EMAIL] and we will delete it.

## 7. Security

What the Software does to protect information, in summary (the Agreement, Sections 9 to 13, 16 and 21, gives the detail and the limits):

- Consoles talk to the Shop server over encrypted connections, and a remote session is encrypted between the two consoles.
- Backups are encrypted by the Shop server when it stores them. The Shop can still read them; there is no passphrase that would stop it (Agreement, Sections 13.1 and 13.2).
- Passwords for signing in to the Software are kept as salted and peppered hashes. A computer's own sign-in password that a Customer gives the Shop with a repair is stored sealed, shown only to the technicians working that job, and each showing is recorded (Agreement, Section 16.6).
- A full card number is not stored: the Software records a card's brand and last four digits, and Square holds the card.
- Diagnostic records are scrubbed on the computer before they are sent to the Shop server.
- Every remote action is attributed to a technician account and recorded in the Shop server's audit log; no screen content or keystrokes are stored.

We do not promise more than this. The Software is pre-release (0.x) software provided as is (Agreement, Sections 21 and 23). The security of each Shop's server - its hardware, disk encryption, physical security, network exposure, accounts and updates - is the Shop's responsibility (Agreement, Sections 12.3 and 12.4).

## 8. Information you send us directly

If you write to us - for example by email to [CONTACT EMAIL] - we receive your email address, your name if you give it, and whatever your message contains. We use it to reply and to deal with what you asked, keep it only as long as we need it for that and for any follow-up, and do not sell it, share it for advertising or use it for marketing. Feedback about the Software may be used to improve it (Agreement, Section 4.4). Please do not send us a Shop's customer data; we do not need it to answer you.

## 9. Requests about information a Shop holds

To see, correct, delete or get a copy of information about you, to stop emails, or to learn who connected to your computer and when, ask the Shop you deal with. It holds that information and the Software gives it the means to act on a request; we hold none of it and cannot reach it (Agreement, Section 20.2). A person a Customer has named on its account can ask the Shop about their own details in the same way.

If you write to us about information a Shop holds, we can only tell you this and point you to the Shop. To stop a Shop's access to your computer, follow Section 18.3 of the Agreement: disconnect from the tray icon, or uninstall.

## 10. International users

The Software can be used anywhere. Because we receive no information through it, we do not transfer anyone's information between countries; the information stays wherever the Shop runs its server, and goes only where the Shop sends it, including to the services in Section 4.4, some of which are in the United States. A Shop that serves people in a place with rules on international transfers is responsible for meeting them. The rest of this section is a plain summary of how some laws relate to us; it is not legal advice, and it does not say that any of these laws applies to us.

### 10.1 European Union and United Kingdom (GDPR and UK GDPR)

For information on a Shop's server, the Shop is the controller and you can exercise your rights - access, correction, erasure, restriction, portability and objection - with the Shop. We are not its processor. For the information you send us directly (Section 8), we are the controller; we rely on our legitimate interest in answering you, and you have the same rights with us by writing to [CONTACT EMAIL]. You may also complain to the data protection authority where you live or work, or, in the United Kingdom, to the Information Commissioner's Office.

### 10.2 California (CCPA, as amended by the CPRA)

We do not sell or share personal information, as the California Consumer Privacy Act defines those words, including for cross-context behavioural advertising. We collect no personal information through the Software. The only personal information we collect is what you send us directly (Section 8): identifiers such as your name and email address, and the content of your message, used to reply and kept as Section 8 says; we collect no sensitive personal information. To the extent the law applies to us, you may ask us what we hold about you and ask us to delete or correct it, by writing to [CONTACT EMAIL], and we will not treat you differently for asking. Information a Shop holds is the Shop's to answer for as the business.

### 10.3 Canada (PIPEDA)

We are accountable for the personal information in our own control, which is only what you send us directly (Section 8). You may ask to see it or have it corrected by writing to [CONTACT EMAIL]. Information a Shop holds is in the Shop's control and requests about it go to the Shop. If you are not satisfied with our answer, you may complain to the Office of the Privacy Commissioner of Canada.

### 10.4 Elsewhere in the United States

Several states have their own privacy laws. The same facts apply: we receive nothing through the Software, we do not sell personal information or use it for targeted advertising, and requests about a Shop's information go to the Shop. The Software contains no advertising or tracking, so there is nothing in it for a browser's Do Not Track or Global Privacy Control signal to switch off.

## 11. Contacting us about this policy

Nycz Software Solutions, [STREET ADDRESS], Hermiston, Oregon 97838, United States. Email: [CONTACT EMAIL].

## 12. Changes to this policy

We change this policy only by publishing a new version with a release, on the Release Feed and beside every console that installs that release, with a new effective date. A release that changes where the Software sends information, or adds a feature that does, updates this policy in that same release; a feature that has not been released is not described here.

END OF POLICY
