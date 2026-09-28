# Zprium Privacy Policy

**Last updated:** September 28, 2026

## 1. Who is responsible

Zprium is a Discord bot operated by **Isaac Dereck Lizana Correa (Dereck Lizana)**, based in **Italy** ("we").
- Privacy contact: **zprium.support@gmail.com**.
- Support server: **https://discord.gg/HcfkxN7TcH**.

Zprium runs on hardware owned by the controller, located in **Italy**. The database, the cache and the artificial intelligence models all run on that machine. We use no cloud AI provider.

## 2. Who this applies to

This policy covers:
- members of Discord servers where Zprium is present;
- administrators who configure it, in Discord or in its web console.

Zprium only processes data in servers where an administrator added it. Each server decides which modules to turn on: **everything beyond the core is off by default**.

## 3. What we process, why, and for how long

**We do not read your message content.** Zprium does not ask Discord for the message content permission. It only sees text when you:
- mention the bot;
- run a command;
- use the "Summarize" action on a message.

We never store that text.

| Data | Purpose | Legal basis | How long |
| :--- | :--- | :--- | :--- |
| Server id, name and language | Know where Zprium is and which language to answer in | Service | Until 30 days after the bot leaves the server |
| Which modules the server enabled and their settings, with the id of the admin who changed them | Apply the configuration the server chose | Service | Same as above |
| Security record (ids of who acts and who is affected, the action and its details; for a quarantine, the roles removed so they can be restored) | Detect and record attacks (mass deletions, raids) and administrative actions, in a tamper-evident log | Legitimate interest (security) | **No automatic deletion yet.** From version 8.0.6, new records store a pseudonym instead of your id, and erasure works by destroying that pseudonym's key (see §6). Archival of records older than 12 months will come later. Until then we handle requests manually |
| Event log (ids in server events, never message text) | Crash recovery and security analysis | Legitimate interest | 30 days |
| Server automations (Z-Flow): definitions, runs (metadata only, never message text) and failures | Run the automations the server creates | Service | Runs: 90 days. Resolved failures: 30 days. Definitions: until the server is purged |
| Esports teams, rosters and scrim results | Organize the server's matches | Service | Until the server is purged |
| Documents staff add to the AI knowledge base, and their vectors | Answer questions with local AI | Service | Until the document is deleted or the server is purged |
| Proposals, notices and jobs of the autonomous engine | Automatic operations the server enabled | Legitimate interest | 90 days after they finish; pending ones are kept until decided or expired |
| Per-member state in the server (id and the data of the modules that use it) | Moderation and server features | Legitimate interest | While a member; deleted 30 days after leaving the server (kept if they come back sooner) |
| Scheduled jobs (for example, reminders); they may include the id of the member concerned | Do later what the server asked for | Service provision | 30 days after they finish |
| Web console session (Discord id and name, server list) | Sign in to the console | Service | 8 hours, or until you sign out |
| Cached AI answers | Avoid repeating work | Service | 30 minutes |

**Full list, generated from the code:** [data per module](https://izkron.github.io/zprium-legal/privacidad-datos-por-modulo.html).

**Artificial intelligence:**
- Zprium's AI (summaries, questions to the knowledge base) runs **only on our machine**, with local models.
- No text is sent to third-party AI services.
- We do not use your data to train models.
- AI-generated answers are labelled as such.

**We do not:**
- advertise or sell data;
- build profiles across servers;
- log members' IP addresses;
- read presence status.

## 4. Who we share data with

- **Discord Inc.:** Zprium works inside Discord, and whatever the bot posts is processed by Discord under its own privacy policy.
- **Cloudflare, Inc.**, once the web console is published on the Internet: console traffic goes through its network (tunnel and attack protection). Cloudflare acts as our processor.
- **Backups kept off the main machine:** they are encrypted on our machine **before** they leave it, with a key only the controller holds. No one else can read them, including the providers that store them. They are kept on:
  - another machine of the controller, in Italy;
  - **Google Drive (Google Ireland Limited)**, as plain storage;
  - **Cloudflare R2**, in the European Union, until we retire it.

  No copy is kept for more than **35 days**.
- **No one else,** except where the law requires it.

**International transfers:**
- Discord and Cloudflare may process data outside the European Economic Area, under the safeguards they provide (standard contractual clauses). Google may store the encrypted backups outside the EEA, under the same safeguards.
- We store the data in **Italy**. The encrypted backups are also held by the providers listed above.

## 5. Security

We apply these measures:
- no exposed database ports;
- secrets kept out of the code;
- server-side console sessions that expire;
- console permissions computed on the server for every request;
- a tamper-evident security log protected by a hash chain;
- automatic purge of a server's data 30 days after the bot leaves it;
- backups encrypted with `age`, kept for 35 days at most, with an automatic test restore every week.

## 6. Your rights

**What you can ask for:**
- access to your data;
- rectification;
- erasure;
- restriction of processing;
- objection;
- portability.

**How to ask:** email **zprium.support@gmail.com** or open a ticket in **the support server (https://discord.gg/HcfkxN7TcH)**, giving your Discord user id. We will ask you to confirm from Discord that the account is yours.

**Deadlines and scope:**
- We answer within **one month**.
- Requests are handled and carried out **only by the controller**, after checking that the account is yours. We tell you when it is done.
- In the security log, which is immutable, no rows are deleted. What is destroyed is the key of your pseudonym, and from then on the rows can no longer be linked to you. Erasure is complete once the backups that still hold that key rotate out, within 35 days at most. We may keep what the security of the service strictly requires (GDPR art. 17(3)).
- **List of erasures.** So that restoring a backup cannot undo your erasure, we keep a minimal list with three items:
  - a fingerprint of your id (HMAC-SHA256), computed with a key that is kept outside the database. Never your id in clear, and without that key the fingerprint cannot be linked to you;
  - the date of the erasure;
  - who carried it out.

  After **any** restore of a backup, and before the bot starts again, every erasure on the list is applied again: the keys and member data from before each erasure are destroyed once more. If you use the bot again after the erasure, you start from scratch and the list does not affect your new data. The list is kept for as long as the service exists, because it is what stops an erasure from being undone and what shows that we handled your request.
- Administrators can delete all of their server's data by removing the bot: it is erased after 30 days.

**Complaints:** you can also complain to the data protection authority of your country. In **Italy** that is the **Garante per la protezione dei dati personali** (https://www.garanteprivacy.it).

## 7. Children

Zprium is not directed at people under the minimum age Discord requires in their country, and does not knowingly collect their data beyond what it needs to work in a server.

## 8. Cookies

The web console uses **a single session cookie**, strictly necessary to sign in. We use no analytics or advertising cookies.

## 9. Changes

If we change this policy, we will announce it in **the support server (https://discord.gg/HcfkxN7TcH)** and update the date above. Changes that reduce your rights will not apply retroactively.
