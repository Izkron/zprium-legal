# Zprium Privacy Policy

**Last updated:** November 15, 2026

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
- answer a Zprium form, such as a verification challenge or an appeal;
- use the "Summarize" action on a message.

We do not store that text, except in three cases explained below: your conversation with `/ai ask` (30 minutes), the questions the knowledge base could not answer (without who asked them), and what you choose to keep in your memory with the AI.

| Data | Purpose | Legal basis | How long |
| :--- | :--- | :--- | :--- |
| Server id, name and language | Know where Zprium is and which language to answer in | Service | Until 30 days after the bot leaves the server |
| Which modules the server enabled and their settings, with the id of the admin who changed them | Apply the configuration the server chose | Service | Same as above |
| Security record (ids of who acts and who is affected, the action and its details; for a quarantine, the roles removed so they can be restored) | Detect and record attacks (mass deletions, raids) and administrative actions, in a tamper-evident log | Legitimate interest (security) | **No automatic deletion yet.** From version 8.0.6, new records store a pseudonym instead of your id, and erasure works by destroying that pseudonym's key (see §6). Archival of records older than 12 months will come later. Until then we handle requests manually |
| Moderation cases, if the server turns on the moderation module. Each case stores: the action (warning, note, timeout, kick or ban), a **pseudonym** of the person it is about and one of the moderator (never either one's Discord ID), the reason the moderator writes, the duration, the date and whether the case was voided. Timeouts, kicks and bans the staff make from Discord, timeouts set by Discord's AutoMod, and the quarantines and kicks made by Aegis, Zprium's protection against attacks, are recorded as cases too. Aegis cases carry a fixed reason (the type of attack and how many actions there were) and cannot be appealed: the server's staff reviews them | Letting the server's staff keep a moderation history, with every action recorded and verifiable | Legitimate interest (the server's safety and order) | **24 months** from the case, then deleted automatically. Also deleted if the bot leaves the server (30 days) |
| Appeals against moderation cases, if the server turns them on. Each appeal stores: its state (pending, accepted or rejected), the dates, a **pseudonym** of you and one of whoever decided it (never either one's Discord ID), and the staff's reply, if they write one. **We do not keep the text of your appeal:** it is posted to the server's appeals channel | Letting you ask the staff to review a case, with their decision recorded | Legitimate interest (the server's safety and order, and your chance to contest a sanction) | The same as its case: **24 months** from the case, and deleted with it. Also deleted if the bot leaves the server (30 days). What is posted in the channel stays there for as long as its staff keeps it |
| AutoMod strikes, if the server turns the module on. Each strike stores: a **pseudonym** of you (never your Discord ID), whether it came from Discord's AutoMod or from a Zprium rule, the type of rule, the time and, if it came from Discord, the number of its entry in the server's audit log. **Never the text of the message** (Zprium does not receive it), the channel or the rule's name | Automatically timing out people who repeatedly break the server's rules | Legitimate interest (the server's safety and order) | **30 days**. They are also deleted if the bot leaves the server (30 days) |
| Verification, if the server turns it on. While you answer a challenge, Zprium keeps the server, your identifier, the kind of challenge and a fingerprint of the accepted answers (**never what you type**), and how many times you failed. When you verify, it keeps the date and a row in the security log with a **pseudonym** of yours, the role you got and the kind of challenge. If you use up your attempts, another such row, with the attempts and the wait. If the server sets a minimum age, your account's age is worked out from your identifier, without keeping anything. If it turns on the kick of members who do not verify, Zprium keeps a scheduled job with your identifier and the date you joined and, if it kicks you, another row with your **pseudonym** and the deadline. During a mass-join attack, it keeps only that the server is under attack, with no data of yours | So the server lets in only people, without leaving Discord | Legitimate interest (the server's security) | The challenge, **10 minutes**, and it is deleted once answered. The failures, the wait the staff chooses after the last one (**24 hours** at most). The date, like each member's state: until 30 days after leaving the server. The security log rows, like that log (§6). The kick's job, until the deadline and 30 days more. The note of the attack, as long as it lasts (**24 hours** at most) |
| Automatic roles, if the server turns the module on. If there is a delay or a retry, a scheduled job with your ID and the time you joined. For each role, security-log rows with a **pseudonym** of yours, the time you joined and the role: that Zprium was about to give it, that Discord accepted it, or that you already had it and who added it could not be confirmed | Give you the roles the server chose and be able to check later what Zprium did | Provision of the service (the scheduled job). Legitimate interest (server security and operation) for the log rows | The job: 30 days after it ends. The rows: like the rest of the security log (§6) |
| Economy, if the server turns the module on: your virtual coin balance, when you last claimed the daily reward, the history of your movements (rewards, transfers, purchases, game prizes and level rewards, with the other member when there is one) and your shop items | So you can earn, send and spend coins in that server without anything getting lost or charged twice | Provision of the service | While the server uses Zprium; deleted on your erasure request or when the server is purged |
| Levels, if the server turns the module on: your XP and level in that server, how many of your messages earned XP, when the last one did and that day's XP | So you can see your progress with `/profile` and the leaderboard with `/levels leaderboard` | Provision of the service | While the server uses Zprium, even if it turns the module off; deleted on your erasure request or when the server is purged |
| Giveaways, if the server turns the module on: whether you entered a giveaway and when; if you win, that you won; if you host one, that you started it | So you can enter and leave, and so the result can be reproduced | Provision of the service | While the server uses Zprium; deleted on your erasure request or when the server is purged (see the limits in §6) |
| Server logs, if the server turns on the logs module. Zprium posts to the channels the staff picks: members joining and leaving (with the account's creation date), when a member verifies or uses up their verification attempts (with the kind of challenge, **never the answer**), when the verification kicks a member who did not verify in time (with the deadline, **never a reason**), deleted or edited messages (author, channel and time; **never the text**), voice channel joins and leaves, channels and roles created, changed or deleted (and who did it), AutoMod rules created, changed or deleted (their name and who did it, never their words), moderation cases and, if the server turns on AutoMod, its strikes | Letting the server's staff see what happens in it and moderate it | Legitimate interest (the server's safety and order) | **Zprium does not keep them:** each event waits in memory for at most 15 minutes until it is posted, and is lost if the bot restarts. What is posted stays in the server's channel for as long as its staff keeps it |
| Event log (ids in server events, never message text) | Crash recovery and security analysis | Legitimate interest | 30 days |
| Server automations (Z-Flow): definitions, runs (metadata only, never message text) and failures | Run the automations the server creates | Service | Runs: 90 days. Resolved failures: 30 days. Definitions: until the server is purged |
| Esports teams, rosters and scrim results | Organize the server's matches | Service | Until the server is purged |
| The server's knowledge base: texts the controller or the staff review and add, with their source, dates and vectors | Answering questions with local AI, citing where each answer comes from | Service | Until they are replaced or deleted, or the server is purged |
| Your conversation with `/ai ask`: your questions and the answers (at most 20 messages) | Letting the AI take into account what you just asked | Service | **30 minutes** after your last question; then it disappears on its own |
| Questions the knowledge base could not answer: the text of the question **without who asked it**, with identifiers, email addresses, phone numbers and other data removed; if it touches health, religion or other special categories, only which kind it was | Knowing what the knowledge base is missing | Legitimate interest (improving the service) | **180 days** after the last time someone asked it |
| Staff notes of `/ai memory`: the text of the note and who saved it | Giving the AI context about the server | Legitimate interest (running the server) | Until the staff deletes it or the server is purged |
| **Your memory with the AI, only if you turn it on** with `/ai mydata`: what you ask it to keep (preferences, context, notes for later), with its kind and version, and your consent | Remembering what you ask it to | **Your consent**, which you can withdraw at any time | Until you delete it or withdraw your consent; if you do not save it again, **365 days** (180 for summaries). A withdrawn consent is deleted after **30 days** |
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
- During a mass-join attack, if the staff turns it on, Aegis can raise the server's verification level and turn on a Discord AutoMod rule that compares your name and nickname with words the staff chooses. Discord does the comparison: Zprium neither reads nor stores your profile. The level and the rule go back to how they were after the time the staff chooses; if the rule blocked you, you can interact again by changing your name or nickname.

**Verification.** If the server turns on Zprium's verification:
- To see the rest of the server, you press "Verify me" and answer a short challenge: a button, picking an emoji, a simple calculation or a question from the staff. Everything happens inside Discord: **no web pages, no third-party captchas and no record of your IP address**.
- When you press it, Zprium looks at what Discord sends with your press (your roles, whether you accepted the server rules, whether you are timed out and whether AutoMod blocked your name), and does not keep it.
- If you answer right, Zprium gives you the role the staff chose. If you fail several times, you wait the time the staff chose before trying again.
- If the server sets a minimum age, a newer account cannot verify until it reaches it, and Zprium tells you from which day you can. The age comes from your Discord identifier: Zprium keeps nothing new.
- During a mass-join attack that Aegis detects, the challenge is harder until the time the staff chose has passed: a simple calculation (or the staff's question), **a single attempt** and accounts of **7 days** at least.
- If the server turns it on, Zprium kicks members who do not verify within the time the staff chose (**24 hours** by default). Before that it tells you by direct message, if yours are open. **It is not a sanction or a moderation case**: you can join again whenever you like. It never kicks the staff, anyone already verified or anyone the staff holds (quarantined or timed out), and if Zprium was down, the time counts from when it came back. Discord keeps in the server's audit log that Zprium kicked you.
- Your answer is compared with the accepted ones and thrown away: Zprium never keeps or posts it.
- Discord keeps in the server's audit log that Zprium gave you the role.

**Automatic roles.** If the server turns the module on, Zprium gives you the roles the staff chose when you join (10 at most).
- It only **adds** roles: it never removes any, including the ones you already had.
- It waits until you finish Discord's membership screening and, if the server uses Zprium's verification, until you pass it (unless the staff chose to give them on join).
- During a mass-join attack that Aegis detects, it waits until the attack ends.
- It never gives a role with staff permissions and never gives roles to people who were already in the server when it was turned on.
- If the staff removes a role Zprium gave you, Zprium does not give it back while you stay in the server; leaving and coming back is a new join.
- Discord keeps in its audit log that Zprium gave you the role, with the reason "Zprium: automatic roles".

**Economy.** Coins are virtual: they are worth no real money and cannot be exchanged for it. Each server has its own and nothing mixes between servers. The server can see the balance leaderboard with `/economy leaderboard`, which shows your name and balance.

**Levels.** If the server turns the levels module on:
- Each time you send a message, Discord tells Zprium. For XP, Zprium only uses **who** sent it, **in which server** and **when**: it does not analyse or store its text. Messages from bots, webhooks and the system do not count.
- A message earns 15 to 25 XP, at most once a minute and up to 500 XP a day (UTC). The server's staff can change those values with `/config` and turn the module off at any time.
- Only messages sent after the module is turned on count.
- Any member of the server can see your level, XP and rank with `/profile` or on `/levels leaderboard` (the top 10). If the server uses the economy, `/profile` also shows your coins and badges. Those answers are shown only to whoever asks and notify no one.
- Each server has its own levels: nothing mixes between servers.
- Turning the module off stops adding XP but does not delete what you had: if it is turned on again, it is still there. It is deleted on your erasure request or when the server is purged.
- If the staff sets rewards, reaching a level can give you a role (never one with staff permissions) or coins of the server's economy, **once per level**. The role appears in Discord's audit log with the reason "Zprium: level N reward" and in our security log; the coins, in the economy's movement history.
- If the staff picks an announcement channel, Zprium posts "🎉 [your name] reached level N" there, **without notifying you**. With no channel picked (the usual case), nothing is announced.

**Giveaways.** If the server turns the giveaways module on:
- You enter by pressing "Enter" and can leave while it is open. Zprium keeps that you entered and when; it keeps no message of yours. Only one entry per person counts.
- **What is published.** The result is posted in the giveaway's channel, which may be public: the winners are **mentioned** (only they are notified), along with the number of participants, the giveaway's seed and a SHA-256 digest of the list of Discord identifiers of those still in the server at the close. The list itself is not published.
- **The digest is not anonymous.** It is an unsalted SHA-256 of Discord identifiers, which are not secret. Someone who knows the possible participants (for example, in a small server) can try lists until one matches and so learn who entered. We do not promise that the digest cannot be linked to you.
- **What can and cannot be checked.** At the start, the SHA-256 of a secret seed is published. At the close, anyone can check that the revealed seed is the committed one and, **if they know the exact list of eligible participants**, recompute the winners with the published algorithm (HMAC-SHA256 of the seed with each identifier). This does not prove that the list included every eligible participant, nor that Zprium did not know its own seed: the bot generates it.
- Giveaways take no payments and no bets. The prize is described and delivered by the server's staff, not by Zprium.

**Music.** While music plays in a voice channel, Zprium keeps in memory the channel and who asked for each song, for the queue and its controls. It is cleared when the channel empties, with `/music leave` or when the bot restarts. Downloaded songs are kept on Zprium's server as a local copy, with no data about you, and deleted after 30 days without being played.

**Server logs.** If the server turns on the logs module, Zprium posts in a staff channel when you join or leave the server, when you verify or use up your verification attempts, when the verification kicks you for not verifying in time, when you join or leave a voice channel, and when one of your messages is deleted or edited. For a message it only gives the author, the channel and the time: **never its text**, which Zprium does not read. If the message was not in the bot's memory, not even the author. Zprium reports nothing that happens in a channel Discord hides from it, and its posts ping nobody. The server's staff reads those logs and keeps or deletes them like any other message in their server. Zprium keeps no copy.

**Full list, generated from the code:** [data per module](https://izkron.github.io/zprium-legal/privacidad-datos-por-modulo.html).

**Artificial intelligence:**
- Zprium's AI (summaries, questions to the knowledge base) runs **only on our machine**, with local models.
- No text is sent to third-party AI services.
- We do not use your data to train models.
- AI-generated answers are labelled as such.
- **Your memory with the AI** is off until you turn it on with `/ai mydata`. Before keeping anything, Zprium checks the text and refuses what looks like a secret or an identifier, data about health, religion, political opinions, sexual orientation, ethnic origin, trade union membership, genetic or biometric data, or financial hardship. The check is automatic and may not catch everything: do not write such data.
- The AI only uses your memory in answers that **only you can see**. Never in a message in a channel.
- We infer nothing about you: the AI only keeps what you ask it to keep.

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
- **Verification.** The challenge and the failures expire on their own: in 10 minutes and in 24 hours at most. The date you verified is deleted 30 days after you leave the server, or when we handle your erasure request. The security log rows work like the rest: they keep a pseudonym, and when we handle your erasure request we destroy its key. The kick's scheduled job is deleted 30 days after it ends, like the other scheduled jobs.
- **Automatic roles.** Security-log rows work like the rest: they keep a pseudonym, and when we handle your erasure request we destroy its key. When we handle your erasure request we also delete the scheduled jobs that were going to give you a role, and none of them can act on that join again, including after a backup restore. If one was running at that moment, it stops before its next step; what Discord had already done (a role already given) is not undone by the erasure: ask the server's staff. If you join again later, that is a new join. Discord's audit log is handled by Discord and the server. If you do not want automatic roles, ask the server's staff: they can remove the role (Zprium does not give it back for that join) or turn the module off.
- **Economy.** When we handle your erasure request we delete your balance, items and movements in every server; in other members' movements with you, we remove your identifier.
- **Levels.** When we handle your erasure request we delete your XP and level in every server, and they do not come back even if we restore a backup.
- **Giveaways.** When we handle your erasure request we delete your entries in every server, remove you from the winners and remove your identifier from the giveaways you hosted, and it does not come back even if we restore a backup. **What Zprium cannot delete:** the participants digest of a giveaway already closed stays as it is and was computed with your identifier if you entered, so it could still be used to check that you entered; and result messages that mention you are in the server's channel, in Discord: to have one deleted, ask its staff.
- **Your memory with the AI.** With `/ai mydata` you can:
  - see it;
  - export it to a file;
  - correct it, by saving the same key again;
  - delete one note or all of it, and withdraw your consent, which deletes it at once.

  Each of those actions is recorded in the security log, without the content. If you ask us for erasure, we delete it in every server and remove your name from the staff notes you saved, and it does not come back even if we restore a backup. Erasure is complete when the backups rotate, within 35 days at most.
- **Your `/ai ask` conversation and unanswered questions.** The conversation disappears on its own after 30 minutes. Unanswered questions do not keep who asked them, so we cannot find them by your identifier. If you wrote something in one that identifies you, tell us and we will review it by hand.
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
