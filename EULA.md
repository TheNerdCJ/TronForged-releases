# TronForged End User License Agreement

Effective [EFFECTIVE DATE]; first published with TronForged release 0.379.0. Each version of this Agreement is published with its release on the Release Feed (Section 1.4) and describes the Software as built at its effective date.

## In short (non-binding summary)

Licensed, not sold, and there is no TronForged cloud: each repair shop (the "Shop") runs its own server and holds its own keys and data, and the author (the "Licensor") operates nothing, receives nothing and can reach nothing. A connected Customer console lets the Shop see and control the computer, including while you are away and before you sign in, with a banner only while the console runs; disconnecting and uninstalling are the only ways out. It repairs, updates and restarts computers, downloads third-party tools under their vendors' terms, lets the Shop read a Customer's backups by default and never deletes a stored backup. It is unsigned 0.x software, provided as is, without warranty; the Licensor's liability is limited. The numbered sections govern.

## Part I - Who is who, and what you are agreeing to

### 1. Parties and definitions

1.1 This End User License Agreement (the "Agreement") is between [LICENSOR LEGAL NAME], of [LICENSOR ADDRESS] (the "Licensor"), author and copyright holder of TronForged, and the person or entity installing or using the Software ("you"). Contact: [CONTACT EMAIL].

1.2 "Shop": a business that installs the Shop server and Technician consoles and deploys Customer consoles onto computers it services; its personnel use the Software under its license, and whoever installs the Shop server or a Technician console acts for the Shop and represents authority to bind it. "Technician": the holder of an account on a Shop server. "Customer": a person or organisation on whose computer a Shop has installed, or asked them to install, a Customer console, and anyone using it (a licensee of that console only, Part III).

1.3 "Software": TronForged - installer and console program, Shop server program, SYSTEM helper service, remote agent service, repair engine, configuration files, Documentation (README, on-screen text, release notes) and updates - but not Third-Party Components. "Console": the Server Console (which installs and administers a Shop server), the Technician console or the Customer console. "Shop server": the server program run by a Shop on its own hardware.

1.4 "Third-Party Components": software, tools, services and content owned by others that the Software embeds, downloads, invokes or connects to (Schedule A and Section 16.4); "Downloaded Tools": those fetched from vendors at run time. "Release Feed": the public GitHub repository TheNerdCJ/TronForged-releases, where the Licensor publishes releases and this Agreement.

1.5 The Licensor is not party to any arrangement between a Shop and its Customers, and neither is the other's agent.

### 2. Acceptance

2.1 Installing, copying, enrolling or using any part of the Software accepts this Agreement; the install screen says so, and a copy is installed beside every console.

2.2 When a Shop installs a Customer console, the acceptance on the install screen is the Customer's, made through the Shop, which must first show the Customer that screen or this Agreement and obtain their agreement; otherwise the Shop answers to the Licensor for that Customer's compliance. An install nobody sees (imaging or headless enrolment) is licensed only if that agreement was obtained before the computer is put into service, and the Shop answers for it as above.

2.3 You must have legal capacity to contract. A person accepting for a household or organisation represents that they may, and accepts for everyone using that computer, so far as applicable law allows.

2.4 The Licensor revises this Agreement only by publishing a revised version with a later release. The governing version is the one accepted under 2.1 and 2.2: for a Shop, at its most recent install, upgrade or manual publication of a release; for a Customer, at the most recent install, reinstall or reconnect, or a later agreement the Shop obtains. The automatic pipeline (Section 6.3) accepts nothing, so the copy beside a console may be later than the version accepted, which remains on the Release Feed.

2.5 If you do not agree, do not install; if installed, uninstall (Section 18.3 for a Customer).

### 3. What TronForged is, and what the Licensor does not do

3.1 TronForged is a self-hosted, white-label platform for computer repair shops: remote management, service desk, backup and imaging, remote access and an automated Windows repair engine. One installer installs one console per computer; it requires administrator rights and elevates itself, and run-without-installing is not offered.

3.2 No cloud, nothing received, nothing reachable. The Licensor operates no cloud, hosted service, account, relay or rendezvous. Every Shop hosts its own server with its own keys; the Licensor holds no key any Shop server trusts and no account on any Shop server, and consoles talk only to that server plus the contacts in Sections 6, 11.4 and 16.4. Nothing in the Software sends telemetry, crash reports or customer data to the Licensor (redacted records go only to the Shop's server, Section 12.2), and the Licensor cannot access, monitor, update, disable or connect to any Shop's server or computers.

3.3 The Licensor therefore makes no commitment about the processing, security, retention, deletion or breach notification of data (those duties are the Shop's), and may stop publishing releases or discontinue the Software at any time without notice, installed copies remaining licensed.

### 4. Ownership and branding

4.1 The Software and all intellectual property rights in it belong to the Licensor and its licensors. It is licensed, not sold; the source code is private and not licensed to you; all rights not expressly granted are reserved.

4.2 Your data is yours: the Licensor claims no rights in anything you create or store with the Software and never receives any of it.

4.3 A Shop may present the consoles it deploys under its own name, logo and icon through the Software's branding surfaces. That is presentation, not authorship, and permits no claim that the Software is the Shop's own; the executables' metadata still names TronForged, and the TronForged name and artwork belong to the Licensor and may be used only to identify the Software.

4.4 Feedback sent to the Licensor may be used without restriction, attribution or obligation.

### 5. Third-Party Components

5.1 Embedded components (Schedule A, Part 1) are distributed unmodified under their own licenses, which prevail over this Agreement where they conflict. Schedule A carries the required notices; each license text is available from the component's own project and from the Licensor on request, and the unmodified source of each Mozilla Public License 2.0 component is available from its upstream project. Windows components the Software drives are used under the computer's Windows license, not distributed.

5.2 Downloaded Tools. The Software bundles no third-party scanners or utilities; it downloads them from their vendors at run time, verifies each against the catalog and refuses one that cannot be verified. Each tool is subject to its vendor's terms, which bind the Shop and the person running it, not the Licensor; some are home-use-only or trial products (Schedule A, Part 2), the Licensor has verified no tool's terms, and vendors control availability.

5.3 The Patch stage installs PowerShell Gallery modules and runs winget with package agreements accepted on the Shop's behalf, including for the computer's OEM update utility; running it accepts those terms. The Software may install the Microsoft-signed .NET Desktop Runtime when missing, and installs no kernel driver.

5.4 The Licensor gives no warranty and accepts no liability for any Third-Party Component or Downloaded Tool.

### 6. Updates and the Release Feed

6.1 Before installing, the installer reads the Release Feed once, anonymously, and if a newer installer is published downloads it, verifies its checksum and hands over to it; the check can be skipped and sends nothing beyond an ordinary HTTPS request. Installed consoles never contact the Release Feed.

6.2 Installed consoles update only from the Shop server's signed catalog, keeping the previous build for rollback. A Customer cannot decline an update short of disconnecting or uninstalling.

6.3 Automatic pipeline, on by default. Unless paused on the Server Console, the Shop server pulls the Release Feed about every six hours, verifies checksums, publishes to a canary ring at once and promotes to the whole fleet after a 24-hour soak with no failed canary report. A Licensor-published release therefore reaches Customer computers with no Shop click unless paused; the Shop is responsible for that choice, for reading release notes, and for what reaches the computers it services.

6.4 Updates may add, change or remove features and may carry a revised Agreement (Section 2.4); none are owed.

## Part II - The Shop's terms

### 7. License to the Shop

7.1 Subject to this Agreement and any commercial terms the Licensor makes available with the Software, the Licensor grants the Shop a non-exclusive, non-transferable license, without right to sublicense except under (c), to: (a) install and run the Server Console and Shop server on computers it controls, for its business of servicing computers; (b) install and run Technician consoles on its personnel's computers, and sign in on Customers' computers as Section 10.7 provides; (c) install Customer consoles on computers it services and let their Customers use them, provided it holds the authority and consent Sections 2 and 9 require; (d) copy release files, including onto imaging templates, as needed for (a) to (c); (e) brand deployed consoles as Section 4.3 allows; (f) use the Documentation.

7.2 The Shop is responsible for every install, console, account, third-party service and release under its server.

### 8. Restrictions

8.1 Except as this Agreement expressly permits, or as applicable law permits despite this clause, you must not, and must not permit anyone to: (a) reverse engineer or otherwise derive the source code; (b) modify, adapt or create derivative works, or alter program files or embedded payload (documented configuration edits are permitted); (c) distribute, sell, rent, lend or host the Software, except Customer consoles under 7.1(c); (d) remove or alter any proprietary notice, metadata, attribution or license text, except through the branding surfaces - and a Shop must leave this Agreement and the Section 5.1 notices in place on every console it deploys; (e) redistribute release files under another name, or represent the Software as your own or as endorsed by the Licensor; (f) use the Software to access, monitor, control or collect data from any computer or network without the authority and consent Section 9 requires; (g) disable, bypass or interfere with the consent prompts, notices, audit records or arming rules of Section 10, or make a session covert (using the controls the Software offers at the computer is not a breach); (h) use a Downloaded Tool contrary to its vendor's terms; (i) use the Software unlawfully, including against export-control law, or where its failure could cause death, injury or severe damage; (j) circumvent a technical limitation.

8.2 A Customer must use the Customer console and the Shop's server only through the functions the console presents, must not try to reach other customers' data or computers, and must not sign in with a technician account.

### 9. Authority, consent and notice on computers the Shop does not own

9.1 Before installing on, enrolling or connecting to any computer, and while it stays connected, the Shop must hold the authority of its owner or authorised user and comply with every law on computer access, interception, monitoring, screen recording and records about identifiable people, in every place where the Shop, the computer and its users are located, including as to other users of the computer. Where a Customer is a business, the Shop must ensure its staff have been given whatever notice they are owed before connecting. The Shop alone determines what authority is required and obtains it.

9.2 The Shop must obtain the Customer's informed agreement to this Agreement and to unattended remote access, collected on screen at enrolment or when the console is later connected. That text says that by connecting the Customer allows the Shop to reach the PC to help, including while the Customer is away and before anyone signs in, and to install Windows updates and restart it; names what arming installs (start-with-Windows, the boot-start agent service, the helper service that answers administrator prompts, and the firewall rules of the same name); states that a notice stays on screen while a technician is connected and before any restart only while the console is running, that there is no on-screen notice while it is closed or before anyone has signed in, and that such a session is logged and reported the next time the console starts; and names the tray item that disconnects, and that start-with-Windows outlives a disconnect. The recorded consent moves with a reinstall; a recorded "No" stays "No". The Shop must not click that consent for a Customer without instruction, enrol a computer whose owner declined, re-enrol a disconnected computer without fresh consent, or ignore a revocation (Section 14).

9.3 The Shop must understand Section 10 and be able to explain it to a Customer. The consent text names the sign-in screen, the boot-start service, the helper service, the firewall rules and the absence of an on-screen notice while the console is not running (Sections 10.2 and 10.4), but it is a disclosure, not a substitute for the Shop's own duty: the Shop must still answer a Customer's questions before connecting, and must tell the Customer anything its own law requires that the text does not carry. The Software's banner, prompts, notices and logs are tools for notice; whether they are sufficient where the Shop operates is the Shop's judgment.

9.4 The Software records the consent click on the computer and an audit row on the Shop server; the Shop must keep whatever records its law requires. Where privacy law applies to the personal data the Shop server holds (Section 12), the Shop is the controller (or business, or the equivalent); the Licensor is neither processor nor service provider.

9.5 Every remote action is attributed to a technician account. Technician accounts must not be shared, must end when a technician leaves, and the Shop controls who may hold one and from where. Sign-in is password-only; there is no default account, break-glass or back door, a password reset requires physical access to the server, and offline sign-in relies only on a server-issued cache earned by a prior online sign-in (fourteen days; wiped after ten wrong attempts).

9.6 On learning a connected computer has changed hands, the Shop must retire the console and not connect again without the new owner's consent.

9.7 The Shop's own terms with Customers must not contradict, and must carry forward, this Agreement's disclosures on unattended access (including before sign-in and while the console is not running), the Shop's ability to read backups, the absence of a backup deletion path, what the console reports (Section 12.2) and the Software's unsigned, pre-release status; the Shop must not represent an unverified or unbuilt feature as available.

### 10. Remote access

10.1 An "attended" session needs a live Yes at the Customer's computer (a prompt names the technician, defaults to No, and is refused if nobody answers); an "unattended" session uses the token the Customer enabled at connection and proceeds without asking anyone, including before Windows sign-in.

10.2 Arming is not optional on a Customer console: a connected Customer computer is armed for unattended access, with no checkbox to switch it off while connected. Connecting also installs a boot-start Windows service ("TronForged Remote Agent"), hosting the agent whenever the console is not running, and the SYSTEM helper service ("TronForgedHelper"), which reaches elevation prompts and the lock and sign-in screens, plus firewall rules named "TronForged Remote Agent". Arming repeats on every launch and about every fifteen minutes, and the self-repair loop re-installs the helper if it is missing. The only ways out are disconnecting and uninstalling.

10.3 What a technician can do. In a session a technician can see and control the screen, keyboard and mouse - including elevation prompts and the lock and sign-in screens where the helper is present - and run repair stages, fixes, Downloaded Tools and reports. The remote command surface is a closed list of named capabilities; there is no free-form command execution. The session is encrypted end to end between the two consoles; the Shop server authenticates it and relays ciphertext it cannot read.

10.4 Notice, and its absence. While the Customer console runs, a banner names any connected technician. When it is not running (before sign-in, after it is closed, or with start-with-Windows off) the agent service hosts the agent, and a technician can connect on the unattended token with no banner and no prompt. Such a session is only logged; when the console next starts it shows a one-time notice naming the technician and time, which is not otherwise guaranteed and is unverified on real hardware (Section 21). The Software has no screen-blanking, notice-muting or hidden-capture feature. The Shop must decide under its own law whether and how to tell the Customer about such work.

10.5 Audited, not recorded. Logs on the computer record arming, each connection, refusal, disconnection and remote command; the Shop server's audit log records each session start and refused join, with the technician's identity. No screen content or keystrokes are stored; other recordings are the Shop's doing.

10.6 A technician with the patch-approval permission may remotely install Windows updates and restart the computer, audited, after an on-screen notice that offers no cancel control: sixty seconds' warning for an immediate restart, or, for a restart when idle, a notice followed by fifteen idle minutes and a two-minute countdown. Scans and installs are skipped on metered connections and on battery. The Shop must not command a restart at a time it knows to be harmful.

10.7 Technician sign-in on a Customer's computer raises that session to a Technician console until sign-out, closing the window or two hours, then removes the cached credential.

### 11. The repair engine, Downloaded Tools and destructive operations

11.1 It changes things. The engine's cleaning, debloating, disinfecting, resetting, software removal, updates and restarts are changes, some irreversible, and its imaging, restore and data-recovery utilities can overwrite disks. It creates a restore point and a registry backup first, can resume after a restart, and gates the most dangerous operations (a whole-machine restore needs a dry-run plan and a typed confirmation, and refuses the running Windows disk), but the decision to run them is yours. The Shop must hold the Customer's authority for the work, take its own backups, and bears the consequences.

11.2 Sensitive material. Optionally, the engine copies the computer's BitLocker recovery keys to its logs folder, recovers product keys and, only on the technician's switch, exports saved Wi-Fi keys in plain text. A forensics collector, when a technician runs it, copies and hashes Windows artifacts - registry hives, browser databases, recycle-bin records and others - into a chain-of-custody bundle without modifying the computer, and on the technician's switch creates a shadow copy. Reports are filed on the computer; service reports attach automatically to tickets on the Shop server. The Shop must treat all of this as confidential Customer material and use it only for the repair.

11.3 The engine restarts after updates and for Safe Mode disinfection; the console's self-repair loop never restarts on its own. The Software adds no antivirus exclusion for itself, and the Shop should not add one on a Customer's computer without the Customer's agreement.

11.4 Besides the Shop server, an installed console contacts tool vendors, Microsoft, the PowerShell Gallery, OEM updaters and GitHub for downloads and, if the Shop enables it, the Shop's SMTP provider - on the Shop's behalf, never the Licensor.

### 12. The Shop server: the only place the data lives

12.1 The Shop server's database holds the Shop's users, console credentials, Customer records, tickets, invoices, the backup catalog, diagnostics, chat presence and an IP-stamped audit log; technicians are data subjects of it too.

12.2 What every console reports, with no opt-out. Each enrolled console sends the Shop server a regular beat (machine name and label, a hashed installation identifier, Windows version, uptime, online and alert state, CPU load and free memory, and about daily its missing Windows updates and pending restart) and redacted diagnostic records (run outcome, stage results, a crash fingerprint and a scrubbed message - never a stack trace - in which paths, share names and email addresses are replaced; a short run-log tail travels only when a run failed). The server keeps daily medians for four hundred days and raw run and tool records for ninety; full crash detail leaves a computer only by a manual Support Bundle. Only disconnecting or uninstalling stops it.

12.3 Not encrypted at rest: password hashes are salted and peppered; everything else is plaintext to whoever can read the database files, the daily unencrypted database snapshots or any manual database backup file, and such a reader can impersonate any console. Disk encryption, physical security and those snapshots and backup files are the Shop's responsibility.

12.4 The Shop server must be reachable on a public address with one forwarded port; Customers never forward anything. Exposing it to the internet is the Shop's decision and risk, and the Shop must keep the server updated.

12.5 The Software deletes no Customer data on its own; the Shop must meet its own retention and deletion duties, by other means where the Software offers none (Section 13.3).

### 13. Backups in the Shop's custody

13.1 Backups are encrypted on the computer before they leave; the Shop server and any destination hold ciphertext only.

13.2 The Shop can read them by default: per-backup keys are wrapped under the server's own secret, so the Shop can restore and read a Customer's backup without the Customer present, and must protect that data and use it only for the Customer's purposes. A Customer may opt in to a passphrase, after which the server cannot read the backups; a lost passphrase is permanent loss unless the audited, opt-in escrow was enabled, and the Licensor cannot recover any key.

13.3 Nothing is deleted. There is deliberately no deletion path for stored backups - retention policies shown in the product are a preview only and delete nothing, the store only grows, and per-Customer quotas are enforced at upload; a deletion request cannot be honoured through the product, and the Shop must remove the data by other means.

13.4 Restores run from inside Windows only. "Boot in VM" runs an image under Hyper-V for inspection only; Windows may report itself unactivated there, and it is not a way to run a Customer's Windows license. The Shop must test the backups it relies on.

### 14. The Customer's controls, which the Shop must leave intact

14.1 The Shop must not remove, hide, misleadingly rename or defeat the Customer's means of seeing and ending its access: the tray icon and its disconnect, start-with-Windows and close items; the disconnect dialog; the attended prompt; the banner and the "while you were away" notice; the force-uninstalls in Settings, Add or Remove Programs and the installer; and the services and firewall rules of Section 10.2.

14.2 On disconnect the console tells the Shop server when reachable and removes the unattended token, the recorded consent, the agent service and the helper; uninstalling removes everything.

### 15. Optional AI features

15.1 AI features are opt-in and default off. A Shop that turns them on supplies an Anthropic API key or a Claude Code sign-in on the Shop server; consoles never call a model. All AI traffic leaves from the Shop server, to Anthropic, under the Shop's own account and Anthropic's terms; the Licensor is not in the chain.

15.2 What is sent: a fleet health summary from the redacted diagnostics of Section 12.2, a draft customer summary from one repair run (used only if a technician approves it), and a numeric server-sizing snapshot. Calls are audited by token count, without content. The optional training export is an explicit administrator action; the training pipeline itself is not in any release and never runs on a Customer's computer.

15.3 A model never acts on a machine: no tools are declared, the command-line route runs with tools disabled, and model output is never parsed or dispatched, only shown, labelled AI-generated. The Shop is responsible for what it sends to its provider, including any personal data in it, and for the provider's terms and cost.

### 16. Payments, accounting, email and the Shop's other services

16.1 Square. Card payments run through Square under the Shop's own account; card numbers never enter the Software, and the Shop's obligations under Square's terms and card-network rules are its own.

16.2 QuickBooks. Export writes Intuit's QuickBooks Desktop (.iif) and QuickBooks Online (.csv) formats; no Intuit software or API is used, nothing syncs, and QuickBooks Online with sales tax has no CSV import path. The Shop is responsible for its books and taxes.

16.3 Email. Invoices go out from the Shop's own SMTP mailbox; engine notifications and support requests use a per-console SMTP setting that ships disabled; messages carry no tracking.

16.4 The Shop server contacts Anthropic, Square, Cloudflare (dynamic DNS), S3-compatible storage, the Shop's SMTP provider and GitHub (anonymously, for releases) only when the Shop configures them, under the Shop's own contracts; the Licensor is not party to any of these.

## Part III - The Customer's terms

For the person whose computer carries the Customer console. Your repair shop (your "Shop") installed it or asked you to; your relationship for the repair work, your data and any complaint is with that Shop, and the Licensor cannot see, stop or reverse anything the Shop does. Sections 8.2 and 21 and Part IV also apply to you.

### 17. Your license

17.1 The Licensor grants you a personal, non-transferable, non-sublicensable license to use the Customer console on the computer it was installed on, to receive services from your Shop, for as long as it stays installed, on these terms. You may not copy it elsewhere or use it to reach other computers.

17.2 The console lets you request support, run curated safe fixes, read reports, back up files where offered, see your tickets, and lets your Shop connect; it is not antivirus, nor a substitute for your own copies of important files. A technician may also sign in on your computer with their own account (Section 10.7).

### 18. Remote access to your computer: what you agreed to, what you will see, how to stop it

18.1 Unattended access. When your computer was connected, you (or someone acting for you) accepted the consent in Section 9.2. From then on your Shop can reach your computer to help you, including when you are away and before you sign in, and can install Windows updates and restart it (with sixty seconds' notice, or after the computer has been idle; Section 10.6); connecting also installed the services in Section 10.2, and none of this can be switched off while connected. Others who use your computer can be seen during a session; tell them.

18.2 What you will and will not see. While the console runs, a banner names any connected technician, and an attended request is a prompt that needs your Yes; unattended access needs no prompt. When the console is not running there is no banner and no prompt - only a log and a one-time notice when the console next starts, not otherwise promised and untested on real hardware (Section 10.4). Nobody gets a recording of your screen, but your Shop can see and control it while connected (Section 10.3) and run tools that read recovery keys, product keys and copies of Windows artifacts including browser databases (Section 11.2).

18.3 How to stop it. Closing the window does not stop the console, and the agent service runs regardless. Your real stops are:

- Disconnect: right-click the tray icon, choose "Connect to my repair shop" (while connected, that item is the disconnect) and confirm Yes. This ends your Shop's access, clears your consent and removes the services.
- Uninstall: Add or Remove Programs, the force-uninstall in Settings (works even if the server is unreachable), or the installer's force-uninstall.

Turning start-with-Windows off, or closing the console, stops the console but not the agent service. Either stop tells your Shop's server; a record of the enrolment remains until the Shop removes it.

18.4 Change of hands. Before you sell, give away, return or dispose of the computer, disconnect or uninstall; until you do, the Shop can still reach it, because the recorded consent stays with the installation, not with you. If you received a computer that carries the console and did not agree to it, or no longer trust the business that installed it, use Section 18.3.

### 19. What the console sends, stores and downloads

19.1 To your Shop, and nobody else. The console sends your Shop the reporting in Section 12.2, technician reports and, if you use it, your backups, encrypted before they leave; no setting turns that off short of disconnecting or uninstalling, and nothing goes to the Licensor or anyone else.

19.2 Downloads. When a repair runs, the console downloads onto your computer, from their vendors, the tools and packages in Sections 5.2, 5.3 and 11.4; Windows and antivirus products may warn about some of them.

19.3 A hidden data folder beside the program holds your Shop's connection details, the unattended-access token (sealed to this computer), your recorded consent, logs, reports and downloaded tools; no password of yours is stored in plain text. If the BitLocker key option was used during a repair, a copy of your recovery key sits in the logs folder; ask your Shop to remove it. When a technician signs in on your computer (Section 10.7), what that session needs about the Shop's other machines is held in memory only, and ending it - by signing out, by the two-hour limit, or by quitting the program - deletes their credential, that list and any unsent notes from your computer.

### 20. Backups and requests about your data

20.1 If you back up to your Shop, it can restore and read those backups by default; for backups only you can open, ask about customer-managed keys (a lost passphrase loses the data; Section 13.2). Nothing in the product deletes a stored backup (Section 13.3); a deletion request to your Shop is met outside it.

20.2 Requests about your data - to see, correct or delete it, or to learn who connected and when - go to your Shop, which holds it; the Licensor holds nothing about you.

## Part IV - Terms that apply to everyone

### 21. Development status, unsigned binaries and known limits

21.1 Unverified on real hardware. At the effective date the features never exercised on real hardware include unattended access before sign-in and while the console is not running (including its notice), remote update installs and restarts, the TLS front door, dynamic DNS, the move from PostgreSQL to the embedded database, desktop-duplication capture and multiple monitors, and Square charges. Only attended remote desktop has been exercised on real hardware; the README's status section controls.

21.2 Not code-signed. Windows SmartScreen warns before running the executables, the elevation prompt shows an unknown publisher, and Smart App Control blocks the file outright (turning Smart App Control off is the computer owner's decision and cannot be reversed without resetting Windows); the publisher name in the file's properties is not a signature. Verify a download against the published SHA-256 checksum before installing, and do not tell a Customer the files are signed.

21.3 Antivirus. The Software installs services, captures the screen, injects input and replaces its own executable; occasional quarantine is expected.

21.4 Not built: bare-metal restore, a web portal, mobile access, backup deletion, maintenance windows, customer chat, two-factor authentication, QuickBooks sync, a scripting library, scheduled patching, voice, service-level contracts. Retired: the portable USB console and the vendor relay.

21.5 Cryptography protects transit and sealed secrets, not the database against an administrator or a stolen disk. Technician team chat is sealed under a shared team passphrase: any technician holding it can read any message and could forge a sender; it is not a system of record.

### 22. Term and termination

22.1 This Agreement takes effect on first install or use and lasts until terminated. A Customer may terminate by uninstalling (Section 18.3); a Shop by uninstalling its server and every console and ceasing use.

22.2 The Licensor may terminate the license of a Shop or Customer that materially breaches this Agreement - in particular Sections 8, 9 and 14 - and does not cure within thirty (30) days of notice, or immediately if the breach cannot be cured. Notice to a Shop goes to any address it has given the Licensor or, if none, takes effect thirty (30) days after publication on the Release Feed and in the next release's notes; a Customer's license terminates only on actual notice. The Licensor cannot remotely disable installed Software.

22.3 On termination the licenses end and you must uninstall. The Licensor holds nothing to return or delete; a Shop remains responsible for the data on its server, and a Shop's termination does not itself terminate a Customer's license. Sections 3.2, 3.3, 4, 5.4, 8, 9.4, 12.5, 13.2, 20.2 and 22.3 to 27 survive termination.

### 23. DISCLAIMER OF WARRANTIES

23.1 THE SOFTWARE, THE DOCUMENTATION AND THE RELEASE FILES ARE PROVIDED "AS IS" AND "AS AVAILABLE", WITH ALL FAULTS AND WITHOUT WARRANTY OF ANY KIND. TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW, THE LICENSOR DISCLAIMS ALL WARRANTIES, CONDITIONS AND REPRESENTATIONS, EXPRESS, IMPLIED OR STATUTORY, INCLUDING MERCHANTABILITY, SATISFACTORY QUALITY, FITNESS FOR A PARTICULAR PURPOSE, TITLE, NON-INFRINGEMENT, ACCURACY AND QUIET ENJOYMENT, AND ANY WARRANTY FROM COURSE OF DEALING OR USAGE.

23.2 WITHOUT LIMITING 23.1, THE LICENSOR DOES NOT WARRANT THAT: (A) THE SOFTWARE WILL BE ERROR-FREE, UNINTERRUPTED, SECURE OR FREE OF HARMFUL COMPONENTS; (B) IT WILL REPAIR ANY COMPUTER, REMOVE ANY MALWARE OR PRESERVE ANY DATA, SETTINGS OR SOFTWARE; (C) ANY BACKUP OR IMAGE CAN BE RESTORED, RETAINED OR DELETED; (D) ANY THIRD-PARTY COMPONENT OR DOWNLOADED TOOL WILL BE AVAILABLE, SAFE OR LICENSED FOR YOUR USE; (E) REMOTE ACCESS WILL BE RELIABLE, OR THAT ANY NOTICE OR AUDIT RECORD WILL APPEAR IN EVERY CIRCUMSTANCE, INCLUDING ON THE SIGN-IN SCREEN, WHILE THE CONSOLE IS NOT RUNNING, OR AFTER A SESSION THAT TOOK PLACE WHILE IT WAS NOT RUNNING; (F) AI-GENERATED OUTPUT WILL BE ACCURATE; (G) SECURITY MEASURES WILL PREVENT UNAUTHORISED ACCESS; (H) ANY FEATURE LISTED AS UNVERIFIED OR NOT BUILT WILL WORK OR EXIST; OR (I) USE OF THE SOFTWARE WILL COMPLY WITH ANY LAW, REGULATION, INDUSTRY STANDARD OR CONTRACT THAT APPLIES TO YOU, INCLUDING PRIVACY, SURVEILLANCE, CONSUMER, TAX, ACCOUNTING AND PAYMENT-CARD REQUIREMENTS.

23.3 THE SOFTWARE IS A TOOL FOR TRAINED TECHNICIANS, NOT A SUBSTITUTE FOR PROFESSIONAL JUDGMENT, TESTED BACKUPS OR LEGAL ADVICE; YOU ASSUME THE ENTIRE RISK OF USING IT, OF RUNNING ANY STAGE, FIX, TOOL, UPDATE OR RESTART ON ANY COMPUTER, AND OF ANY RESULT. THE LICENSOR PROVIDES NO SUPPORT, MAINTENANCE, HOSTING, UPTIME, DATA-PROCESSING, DATA-SECURITY OR BREACH-NOTIFICATION SERVICE. NO ADVICE FROM THE LICENSOR, THE DOCUMENTATION OR ANY SHOP CREATES A WARRANTY; A SHOP'S PROMISES TO ITS CUSTOMERS ARE THE SHOP'S ALONE.

23.4 WHERE APPLICABLE LAW DOES NOT ALLOW THESE EXCLUSIONS, THEY APPLY TO THE FULLEST EXTENT PERMITTED, ANY IMPLIED WARRANTY THAT CANNOT BE EXCLUDED IS LIMITED TO THE SHORTEST PERIOD THE LAW PERMITS, AND NOTHING HERE LIMITS ANY CONSUMER RIGHT THAT CANNOT BE LIMITED BY CONTRACT.

### 24. LIMITATION OF LIABILITY

24.1 TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW, IN NO EVENT WILL THE LICENSOR OR ITS OWNERS, CONTRIBUTORS, SUPPLIERS OR LICENSORS BE LIABLE TO YOU OR ANY THIRD PARTY FOR ANY INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, PUNITIVE OR CONSEQUENTIAL DAMAGES, OR FOR ANY LOSS OF DATA, USE, PROFITS, REVENUE, BUSINESS OR GOODWILL, COST OF SUBSTITUTE GOODS OR SERVICES OR DATA RECOVERY, COMPUTER FAILURE, OR UNAUTHORISED ACCESS TO DATA, ARISING OUT OF THIS AGREEMENT OR THE SOFTWARE, UNDER ANY THEORY OF LIABILITY (INCLUDING NEGLIGENCE), EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGES OR IF A REMEDY FAILS OF ITS ESSENTIAL PURPOSE.

24.2 TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW, THE LICENSOR'S TOTAL CUMULATIVE LIABILITY TO YOU AND ALL PERSONS CLAIMING THROUGH YOU, ARISING OUT OF THIS AGREEMENT OR THE SOFTWARE, WILL NOT EXCEED THE GREATER OF (A) THE AMOUNTS YOU PAID THE LICENSOR FOR THE SOFTWARE IN THE TWELVE (12) MONTHS BEFORE THE CLAIM AROSE AND (B) ONE HUNDRED UNITED STATES DOLLARS (USD 100). A CUSTOMER'S REMEDIES FOR SERVICES PERFORMED ON ITS COMPUTER LIE AGAINST ITS SHOP.

24.3 WITHOUT LIMITING 24.1 AND 24.2, THE LICENSOR IS NOT LIABLE FOR ANY ACT OR OMISSION OF A SHOP, A CUSTOMER OR ANY THIRD PARTY; FOR ANY REMOTE ACCESS, REPAIR, RESTART, WIPE, IMAGING OR RESTORE PERFORMED WITH THE SOFTWARE, INCLUDING WITHOUT AUTHORITY OR CONSENT; FOR ANY DATA A SHOP HOLDS, LOSES, DISCLOSES OR FAILS TO DELETE; FOR THE SECURITY OF A SHOP'S SERVER OR NETWORK; OR FOR ANY UNVERIFIED OR UNBUILT FEATURE.

24.4 NOTHING IN THIS AGREEMENT EXCLUDES OR LIMITS LIABILITY THAT CANNOT BE EXCLUDED OR LIMITED UNDER APPLICABLE LAW, INCLUDING FOR DEATH OR PERSONAL INJURY CAUSED BY NEGLIGENCE, FRAUD, OR ANY NON-WAIVABLE CONSUMER RIGHT.

24.5 To the extent applicable law permits, any claim arising out of this Agreement or the Software must be brought within one (1) year after it accrues.

### 25. Infringement claims

If a third party claims that the Software, as delivered and used as permitted, infringes its intellectual property, the Licensor may at its option and expense modify or replace the affected part, obtain the right for you to continue using it, or terminate the license for it and refund any prepaid license fee for the unexpired period. This is the Licensor's entire liability, and your sole remedy, for infringement claims; it does not cover Third-Party Components, Downloaded Tools, a Shop's branding, data or modifications, or use contrary to this Agreement.

### 26. Indemnity by the Shop

26.1 The Shop will defend, indemnify and hold harmless the Licensor and its owners, contributors and suppliers from all claims, losses, liabilities, fines, costs and expenses (including reasonable legal fees) arising out of: (a) any access to or action on a computer or network by or through the Shop's server or consoles, including any claim that authority or consent was lacking; (b) the Shop's handling or loss of data, including any security incident; (c) its breach of Sections 8 to 14; (d) its use of any Downloaded Tool, Third-Party Component or third-party service; (e) its promises to Customers and its branding or marketing of the Software; (f) any operation performed with the Software; or (g) its payments, accounting or tax practices - except to the extent a claim arises from the Licensor's fraud or wilful misconduct.

26.2 The Licensor will notify the Shop promptly of a claim, let it control the defence and cooperate reasonably at the Shop's expense; the Shop may not settle a claim in a way that binds the Licensor without its written consent.

### 27. General

27.1 Governing law and venue. This Agreement is governed by the laws of [GOVERNING LAW], without regard to conflict-of-laws rules, and the parties submit to the exclusive jurisdiction of the courts of [VENUE], except that the Licensor may seek equitable relief anywhere to protect its intellectual property, and nothing here deprives a consumer of the mandatory protections or courts of their home jurisdiction. The UN Convention on Contracts for the International Sale of Goods does not apply.

27.2 Entire agreement. This Agreement, its Schedule and the third-party notices and commercial terms it references are the entire agreement between you and the Licensor about the Software and supersede all prior communications.

27.3 Severability; waiver. An unenforceable provision is enforced to the maximum extent permissible and the rest stands; failure to enforce is not a waiver, and no waiver is effective unless in writing.

27.4 Assignment. You may not assign this Agreement, by operation of law or otherwise, without the Licensor's written consent, except that a Shop may transfer its license with substantially all of its business on written notice; a prohibited assignment is void. The Licensor may assign to a successor.

27.5 Notices to the Licensor go to [CONTACT EMAIL] or [LICENSOR ADDRESS]; to a Shop, to any email address it has given the Licensor or by publication on the Release Feed and in the next release's notes (subject to Section 22.2).

27.6 Relationship. The parties are independent contractors; nothing here creates a partnership, joint venture, agency or franchise, and a Shop may not represent that it is the Licensor's agent, partner or reseller. There are no third-party beneficiaries, except that authors of Third-Party Components may enforce their licenses.

27.7 Export. The Software contains encryption; you must comply with applicable export-control and sanctions laws, and a Shop represents that it is not a sanctioned person and is not in a sanctioned country.

27.8 Interpretation. The English text controls; headings are for convenience; "including" means "including without limitation". This Agreement governs the parties' rights regardless of on-screen wording (a label that differs from this Agreement's description denotes the equivalent surface); its descriptions of the Software are given without warranty (Section 23), and the Software as shipped governs what it does.

## Schedule A - Third-Party Components

License names are as the Licensor reads each package's metadata; the component's own license file controls, and "as stated by its vendor" marks an item the Licensor has not verified.

### Part 1 - Distributed inside the Software

- Microsoft .NET runtime (.NET Framework 4.8 carrier; .NET 10 payload): MIT; .NET Framework under Windows terms.
- LibreHardwareMonitorLib, DiskInfoToolkit, RAMSPDToolkit-NDD and BlackSharp.Core: Mozilla Public License 2.0, unmodified; source upstream.
- HidSharp and SQLitePCLRaw: Apache License 2.0.
- Microsoft .NET support libraries (System.* packages), Microsoft.Data.Sqlite and System.Security.Cryptography.ProtectedData: MIT.
- SQLite native engine: public domain, as stated by its authors.
- Npgsql (retiring; still ships): PostgreSQL License.
- Mono.Posix.NETStandard (declared dependency; if shipped) and the PostgreSQL server binaries (only on Shop servers set up before release 0.368): License as stated by its vendor.

### Part 2 - Downloaded at run time from their vendors (never distributed)

The Downloaded Tools are those the Software's tool catalog names at the installed version: malware scanners and removers; uninstallers; hardware, disk, recovery, cleaning, driver and network utilities; the PSWindowsUpdate and Microsoft.WinGet.Client modules and winget; the Dell, Lenovo and HP update utilities (Section 5.3); the Microsoft .NET Desktop Runtime installer; and Windows installation media via Fido and Rufus - each under its vendor's terms (Section 5.2). Flagged: Dr.Web CureIt! (home use only); HitmanPro and Hard Disk Sentinel (trials); TDSSKiller (discontinued); Kaspersky Virus Removal Tool (not available in the United States). PawnIO is offered as an optional driver the Software never installs.

END OF AGREEMENT
