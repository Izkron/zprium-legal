# Zprium Privacy Policy

**Last updated:** October 10, 2026

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
| Moderation cases, if the server turns on the moderation module. Each case stores: the action (warning, note, timeout, kick or ban), a **pseudonym** of the person it is about and one of the moderator (never either one's Discord ID), the reason the moderator writes, the duration, the date and whether the case was voided. Timeouts, kicks and bans the staff make from Discord, timeouts set by Discord's AutoMod, and the quarantines and kicks made by Aegis, Zprium's protection against attacks, are recorded as cases too. Aegis cases carry a fixed reason (the type of attack and how many actions there were) and cannot be appealed: the server's staff reviews them | Letting the server's staff keep a moderation history, with every action recorded and verifiable | Legitimate interest (the server's safety and order) | **24 months** from the case, then deleted automatically. Also deleted if the bot leaves the server (30 days) |
| Appeals against moderation cases, if the server turns them on. Each appeal stores: its state (pending, accepted or rejected), the dates, a **pseudonym** of you and one of whoever decided it (never either one's Discord ID), and the staff's reply, if they write one. **We do not keep the text of your appeal:** it is posted to the server's appeals channel | Letting you ask the staff to review a case, with their decision recorded | Legitimate interest (the server's safety and order, and your chance to contest a sanction) | The same as its case: **24 months** from the case, and deleted with it. Also deleted if the bot leaves the server (30 days). What is posted in the channel stays there for as long as its staff keeps it |
| AutoMod strikes, if the server turns the module on. Each strike stores: a **pseudonym** of you (never your Discord ID), whether it came from Discord's AutoMod or from a Zprium rule, the type of rule, the time and, if it came from Discord, the number of its entry in the server's audit log. **Never the text of the message** (Zprium does not receive it), the channel or the rule's name | Automatically timing out people who repeatedly break the server's rules | Legitimate interest (the server's safety and order) | **30 days**. They are also deleted if the bot leaves the server (30 days) |
| Server logs, if the server turns on the logs module. Zprium posts to the channels the staff picks: members joining and leaving (with the account's creation date), deleted or edited messages (author, channel and time; **never the text**), voice channel joins and leaves, channels and roles created, changed or deleted (and who did it), AutoMod rules created, changed or deleted (their name and who did it, never their words), moderation cases and, if the server turns on AutoMod, its strikes | Letting the server's staff see what happens in it and moderate it | Legitimate interest (the server's safety and order) | **Zprium does not keep them:** each event waits in memory for at most 15 minutes until it is posted, and is lost if the bot restarts. What is posted stays in the server's channel for as long as its staff keeps it |
| Event log (ids in server events, never message text) | Crash recovery and security analysis | Legitimate interest | 30 days |
| Server automations (Z-Flow): definitions, runs (metadata only, never message text) and failures | Run the automations the server creates | Service | Runs: 90 days. Resolved failures: 30 days. Definitions: until the server is purged |
| Esports teams, rosters and scrim results | Organize the server's matches | Service | Until the server is purged |
| Documents staff add to the AI knowledge base, and their vectors | Answer questions with local AI | Service | Until the document is deleted or the server is purged |
| Proposals, notices and jobs of the autonomous engine | Automatic operations the server enabled | Legitimate interest | 90 days after they finish; pending ones are kept until decided or expired |
| Per-member state in the server (id and the data of the modules that use it) | Moderation and server features | Legitimate interest | While a member; deleted 30 days after leaving the server (kept if they come back sooner) |
| Scheduled jobs (for example, reminders); they may include the id of the member concerned | Do later what the server asked for | Service provision | 30 days after they finish |
| Web console session (Discord id and name, server list) | Sign in to the console | Service | 8 hours, or until you sign out |
| Cached AI answers | Avoid repeating work | Service | 30 minutes |

**Moderation notices.** If a moderator warns you, times you out or kicks you with Zprium, the server may send you a direct message with the action, the reason and the duration. It **never says who did it**. Staff-only notes are never sent to you. These notices are on by default, and each server can turn them off.

**Appeals.** If the server has appeals turned on, the direct message that tells you of a warning, a timeout or a kick includes a button to appeal for **14 days**.
- You write why you think the case should be reviewed.
- Zprium posts it in a private staff channel of the server, together with your Discord name and the case. It does not keep that text: you keep a copy in the direct message.
- The staff decides. We tell you by direct message, **without saying who decided**, and you can check the state at any time with the same button.
- You can appeal each case **once**, and at most **3 cases every 30 days** in each server.
- Staff-only notes cannot be appealed, because they are never sent to you.

**AutoMod.** If the server turns on Zprium's AutoMod module:
- When Discord's AutoMod blocks a message of yours, Zprium learns it from the server's audit log: who, when and what type of rule. **Never what the message said.**
- Zprium also counts, without reading them, how many messages you send within a few seconds and how many people or roles you mention in a message. Those counts last less than a minute and are not stored.
- Each of those facts is a **strike**. If you collect several in a short time, Zprium **times you out** for a while automatically. By default: 3 in an hour, 10 minutes; 5 in a day, one hour; 8 in a week, one day. Each server can change these values.
- The timeout opens a moderation case. As with any timeout, we tell you by direct message and **you can appeal it**, if the server has notices and appeals turned on.
- If the server keeps moderation logs, each strike shows in its log channel: who, the channel and the type of rule, never the text. So do the messages Discord's AutoMod flags for the staff and the profiles it quarantines, with the rule's name.
- If the server turns it on, Zprium also creates and maintains Discord AutoMod rules on behalf of its staff (invites, links, words and others). The words of those rules are stored in Discord, not in Zprium: Zprium only keeps which rule is its own, a fingerprint to tell whether someone changed it, and the date.
- Zprium's AutoMod never kicks or bans anyone.
- Zprium's strikes and automatic timeouts do not apply to the server's staff.

**Aegis.**
- If the server has a log channel, when Aegis detects an attack it posts there what it did and mentions the person it attributes the attack to. In monitor mode it does nothing: it posts what it would have done in enforce mode, unless the staff turns those reports off.

**Server logs.** If the server turns on the logs module, Zprium posts in a staff channel when you join or leave the server, when you join or leave a voice channel, and when one of your messages is deleted or edited. For a message it only gives the author, the channel and the time: **never its text**, which Zprium does not read. If the message was not in the bot's memory, not even the author. Zprium reports nothing that happens in a channel Discord hides from it, and its posts ping nobody. The server's staff reads those logs and keeps or deletes them like any other message in their server. Zprium keeps no copy.

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
- **Moderation cases.** They work like the security log: they store a pseudonym, not your ID. When we act on your erasure request we destroy the key behind that pseudonym, and from then on your cases can no longer be linked to you. The case itself (the action and its date) is kept until it is 24 months old, for the server's legitimate interest in its history (Art. 17(3) GDPR).
  - The reason is free text. If a moderator wrote your name in it without mentioning you, that name may remain in the text: tell us in your request and we will review it by hand.
  - A moderator cannot delete a case, only void it with a reason.
- **Appeals.** They work like cases: they store pseudonyms, and when we act on your erasure request we destroy their key, so your appeals can no longer be linked to you. They are deleted with their case.
  - The text of your appeal is not in our systems but in the server's appeals channel. To have it deleted, ask its staff; if they do not act on it, write to us and we will pass it on to the server.
  - The staff's reply is free text. If someone on the staff wrote your name in it without mentioning you, that name may remain in the text: tell us in your request and we will review it by hand.
- **AutoMod strikes.** They store pseudonyms, like cases. But those that come from Discord's AutoMod also store the number of their entry in the server's audit log, where Discord does show who it was. So when we act on your erasure request we **delete your strikes**, as well as destroying your key. Otherwise they are deleted after 30 days.
- **Server logs.** Zprium does not keep the logs it posts, so there is nothing to delete in our systems. The posts are in the server's channel: to have one deleted, ask its staff. If they do not act on it, write to us and we will pass it on to the server.
- **List of erasures.** So that restoring a backup cannot undo your erasure, we keep a minimal list with three items:
  - a fingerprint of your id (HMAC-SHA256), computed with a key that is kept outside the database. Never your id in clear, and without that key the fingerprint cannot be linked to you;
  - the date of the erasure;
  - who carried it out.

  After **any** restore of a backup, and before the bot starts again, every erasure on the list is applied again: the keys, member data and AutoMod strikes from before each erasure are destroyed once more. If you use the bot again after the erasure, you start from scratch and the list does not affect your new data. The list is kept for as long as the service exists, because it is what stops an erasure from being undone and what shows that we handled your request.
- Administrators can delete all of their server's data by removing the bot: it is erased after 30 days.

**Complaints:** you can also complain to the data protection authority of your country. In **Italy** that is the **Garante per la protezione dei dati personali** (https://www.garanteprivacy.it).

## 7. Children

Zprium is not directed at people under the minimum age Discord requires in their country, and does not knowingly collect their data beyond what it needs to work in a server.

## 8. Cookies

The web console uses **a single session cookie**, strictly necessary to sign in. We use no analytics or advertising cookies.

## 9. Changes

If we change this policy, we will announce it in **the support server (https://discord.gg/HcfkxN7TcH)** and update the date above. Changes that reduce your rights will not apply retroactively.
